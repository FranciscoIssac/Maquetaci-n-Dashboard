<script setup>
import Bell from "../components/icons/Bell.vue";
import Mail from "../components/icons/Mail.vue";
import Header from "../components/Header.vue";
import HeaderLine from "../components/HeaderLine.vue";
import TestBread from "../components/TestBread.vue";
import UserButton from "../components/UserButton.vue";
import Tablero from "@/components/Tablero.vue";
import Footer from "@/components/Footer.vue";
import SubjectHeader from "@/components/SubjectHeader.vue";
import SubjectCard from "@/components/SubjectCard.vue";
import CalendarioResumen from "@/components/CalendarioResumen.vue";
</script>

<template>
  <div id="background">
    <div id="header">
      <Header></Header>
      <div class="space"></div>
      <HeaderLine></HeaderLine>
    </div>

    <div id="sub-header">
      <TestBread>
        <template #first>Inicio</template>
      </TestBread>
      <div id="user">
        <Mail></Mail>
        <Bell></Bell>
        <UserButton>
          <template #user>Administrador</template>
        </UserButton>
      </div>
    </div>

    <div id="content">
      <div style="display: flex">
        <Tablero id="tablero" height="638px">
          <template #header-title>Guia</template>
        </Tablero>
        <div id="right-content" style="display: flex; flex-direction: column">
          <div style="display: block">
            <h1 id="title" style="margin-top: -7px">Subir material</h1>
            <CalendarioResumen
              id="calendarioresumen"
              style="
                width: 841px;
                height: 208px;
                margin-bottom: 35px;
                margin-top: 18px;
              "
            >
            </CalendarioResumen>
            <SubjectHeader style="height: 36px">
              <template #materia>Materia</template>
              <template #descripcion>Descripcion de la materia</template>
            </SubjectHeader>
            <SubjectCard
              style="margin-top: 10px; margin-bottom: 9px; height: 156px"
            >
              <template #materia>Interfaces Gráficas</template>
              <template #descripcion>
                No. Estudiantes - 22<br />
                Hora clase - 11am<br />
                Progreso - 50.2%<br />
                Tema actual - Punteros
              </template>
            </SubjectCard>
            <SubjectCard style="height: 156px">
              <template #materia>Motores Gráficos</template>
              <template #descripcion>
                No. Estudiantes - 20<br />
                Hora clase - 9am<br />
                Progreso - 70.2%<br />
                Tema actual - Unity
              </template>
            </SubjectCard>
          </div>
        </div>
      </div>
    </div>
    <div id="footer">
      <Footer></Footer>
    </div>
  </div>
</template>

<style scoped>
@media (min-width: 1024px) {
  #right-content {
    width: 825px;
  }

  #tablero {
    margin-right: 18px;
    height: 665px;
  }

  #title {
    color: #000;
    height: 44px;
    font-family: "Open Sans";
    font-size: 32px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
  }

  #content {
    display: flex;
    padding: 16px 102px 80px 101px;
    justify-content: center;
    align-items: center;
    background: var(--Background, linear-gradient(180deg, #bec7d3 0%, #fff 0%));
  }

  #header > .space {
    height: 20px;
    width: 100%;
  }

  #sub-header {
    display: flex;
    justify-content: space-between;
    padding: 10px 40px;
    border-bottom: 2px double black;

    & #user {
      display: flex;
      width: 22%;
      justify-content: space-between;
      align-items: center;
    }
  }
  #backgorund {
    background: var(
      --Background,
      linear-gradient(180deg, #bec7d3 0%, #fff 50%)
    );
  }
}
@media (min-width: 768px) and (max-width: 1024px) {
  #right-content {
    width: max-content;
  }
  #calendarioresumen {
    display: none;
  }
  #tablero {
    display: none;
  }

  #title {
    display: none;
  }

  #content {
    display: flex;
    padding: 16px 102px 80px 101px;
    justify-content: center;
    align-items: center;
    background: var(--Background, linear-gradient(180deg, #bec7d3 0%, #fff 0%));
  }

  #header > .space {
    height: 20px;
    width: 100%;
  }

  #sub-header {
    display: flex;
    justify-content: space-between;
    padding: 10px 40px;
    border-bottom: 2px double black;

    & #user {
      display: flex;
      width: 22%;
      justify-content: space-between;
      align-items: center;
    }
  }
  #backgorund {
    background: var(
      --Background,
      linear-gradient(180deg, #bec7d3 0%, #fff 50%)
    );
  }
}
@media (max-width: 768px) {
  #right-content {
    width: max-content;
  }

  #calendarioresumen {
    display: none;
  }
  #tablero {
    display: none;
  }

  #title {
    display: none;
  }

  #content {
    display: flex;
    padding: 16px 102px 80px 101px;
    justify-content: center;
    align-items: center;
    background: var(--Background, linear-gradient(180deg, #bec7d3 0%, #fff 0%));
  }

  #header > .space {
    height: 20px;
    width: 100%;
  }

  #backgorund {
    background: var(
      --Background,
      linear-gradient(180deg, #bec7d3 0%, #fff 50%)
    );
  }
  #sub-header {
    margin: auto;
    & #testbread {
      display: none;
    }
  }
}
</style>
