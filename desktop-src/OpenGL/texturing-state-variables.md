---
title: Variáveis de estado texturing
description: Variáveis de estado texturing
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variáveis de estado texturing OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff468c701100cc598a519ed3aa290913016a559e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908644"
---
# <a name="texturing-state-variables"></a>Variáveis de estado texturing

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Textura GL \_ *x*</dt> <dd> 

| Propriedade | Valor |
|------------------|-------------------------------------------------------|
| Descrição:     | True se *x* -d texturing habilitado (*x* for 1-D ou 2-d) |
| Grupo de atributos: | textura/Habilitar                                        |
| Valor inicial:   | GL \_ falso                                             |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_textura GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------|
| Descrição:     | imagem de textura *x* -D no nível de detalhe *i* |
| Grupo de atributos: |                                              |
| Valor inicial:   |                                              |
| Comando Get:     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_largura da textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------|
| Descrição:     | largura *da imagem* de textura *x* -D                       |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_altura da textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------|
| Descrição:     | altura *da imagem* de textura *x* -D                      |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_borda de textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------|
| Descrição:     | borda *da imagem* de textura *x* -D                      |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_componentes de textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------|
| Descrição:     | Componentes de imagem de textura                                 |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 1                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_cor da \_ borda da textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------------|
| Descrição:     | Cor da borda da textura                           |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | 0, 0, 0, 0                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_filtro de \_ mínimo de textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------------|
| Descrição:     | Função de minificação de textura                  |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ mais próximo \_ MIPMAP \_ linear                    |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_ \_ filtro mag de textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------------|
| Descrição:     | Função de ampliação de textura                 |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ linear                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>Encapsule a textura do GL \_ \_ \_ *x*</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------------|
| Descrição:     | Modo de quebra de textura (*x* é S ou T)              |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ repetir                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>modo do GL \_ Texture \_ env \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Função de aplicativo de textura         |
| Grupo de atributos: | textura                              |
| Valor inicial:   | GL \_ modular                         |
| Comando Get:     | [**glGetTexEnviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>cor do GL \_ Texture \_ env \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Cor do ambiente de textura            |
| Grupo de atributos: | textura                              |
| Valor inicial:   | 0, 0, 0, 0                           |
| Comando Get:     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>A \_ textura GL \_ Gen \_ *x*</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------|
| Descrição:     | Texgen está habilitado (*x* é S, T, R ou Q) |
| Grupo de atributos: | textura/Habilitar                           |
| Valor inicial:   | GL \_ falso                                |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_plano de olho GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Coeficientes da equação do plano Texgen   |
| Grupo de atributos: | textura                              |
| Valor inicial:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_plano de objeto GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Coeficientes lineares de objeto Texgen    |
| Grupo de atributos: | textura                              |
| Valor inicial:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>modo do GL \_ Texture \_ Gen \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------|
| Descrição:     | Função usada para texgen             |
| Grupo de atributos: | textura                              |
| Valor inicial:   | olho do GL \_ \_ linear                      |
| Comando Get:     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




