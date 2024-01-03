<script setup lang="ts">
import { AtomsButton } from '@/components/Atoms/Button/index'
import { MoleculesContainer } from '@/components/Molecules/Container/index'
import {
  MoleculesCard,
  MoleculesCardBody,
  MoleculesCardFooter,
  MoleculesCardGroup,
  MoleculesCardHeader
} from '@/components/Molecules/Card/index'
</script>

<template>
  <MoleculesContainer size="lg">
    <AtomsButton> Button </AtomsButton>

    <MoleculesCardGroup :list="[{}, {}]">
      <MoleculesCard>
        <MoleculesCardHeader>
          <p style="text-align: center">HEADER</p>
        </MoleculesCardHeader>
        <MoleculesCardBody>
          <p style="text-align: center">BODY</p>
        </MoleculesCardBody>
        <MoleculesCardFooter>
          <p style="text-align: center">FOOTER</p>
        </MoleculesCardFooter>
      </MoleculesCard>
    </MoleculesCardGroup>
  </MoleculesContainer>
</template>

<style>
.box {
  background-color: aquamarine;
  width: 100px;
  height: 50px;
  transition: width 0.8s;
  /* position: absolute; */
}

button:hover + .box {
  width: 300px;
}
</style>
