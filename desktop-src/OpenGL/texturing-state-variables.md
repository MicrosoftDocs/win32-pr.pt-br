---
title: Variáveis de Estado de Texturização
description: Variáveis de Estado de Texturização
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variáveis de estado de texto OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7393fc6e700b028ba3783e5c78d8175e0c3fba4937bf3830d5cae8897aa0d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776576"
---
# <a name="texturing-state-variables"></a>Variáveis de Estado de Texturização

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>TEXTURA \_ GL \_ *x*</dt> <dd> 

| Propriedade | Valor |
|------------------|-------------------------------------------------------|
| Descrição:     | True se *x* – D texturing enabled (*x* é 1D ou 2D) |
| Grupo de atributos: | textura/habilitar                                        |
| Valor inicial:   | GL \_ FALSE                                             |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------|
| Descrição:     | *x* – Imagem de textura D no nível de detalhe *i* |
| Grupo de atributos: |                                              |
| Valor inicial:   |                                              |
| Comando Get:     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>LARGURA \_ DA TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------|
| Descrição:     | *x* – largura da imagem de *textura D*                       |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>ALTURA \_ DA TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------|
| Descrição:     | *x* – altura da imagem de textura *D*                      |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>BORDA \_ DE TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------|
| Descrição:     | *x* – borda de *i da imagem* de textura D                      |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>COMPONENTES \_ DE TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------|
| Descrição:     | Componentes de imagem de textura                                 |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 1                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>COR DA \_ BORDA \_ DA TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------------|
| Descrição:     | Cor da borda da textura                           |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | 0, 0, 0, 0                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>FILTRO MIN \_ \_ DE TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------------|
| Descrição:     | Função de minificação de textura                  |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ NEAREST \_ MIPMAP \_ LINEAR                    |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>FILTRO GL \_ TEXTURE \_ MAG \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------------|
| Descrição:     | Função de ampliação de textura                 |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ LINEAR                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL \_ TEXTURE \_ WRAP \_ *x*</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------------|
| Descrição:     | Modo de quebra de textura (*x* é S ou T)              |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ REPEAT                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>MODO DE \_ ENV DE \_ TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Função de aplicativo de textura         |
| Grupo de atributos: | textura                              |
| Valor inicial:   | GL \_ MODULARTE                         |
| Comando Get:     | [**glGetTexEn ltda**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>COR DE \_ \_ ENV DE TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Cor do ambiente de textura            |
| Grupo de atributos: | textura                              |
| Valor inicial:   | 0, 0, 0, 0                           |
| Comando Get:     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ TEXTURE \_ GEN \_ *x*</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------|
| Descrição:     | O Texgen está habilitado (*x* é S, T, R ou Q) |
| Grupo de atributos: | textura/habilitar                           |
| Valor inicial:   | GL \_ FALSE                                |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>PLANO \_ DE OLHO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Coeficientes de equação do plano de Texgen   |
| Grupo de atributos: | textura                              |
| Valor inicial:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>PLANO \_ DE \_ OBJETO GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Coeficientes lineares do objeto Texgen    |
| Grupo de atributos: | textura                              |
| Valor inicial:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>MODO GL \_ TEXTURE \_ \_ GEN</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Função usada para o texgen             |
| Grupo de atributos: | textura                              |
| Valor inicial:   | GL \_ EYE \_ LINEAR                      |
| Comando Get:     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




