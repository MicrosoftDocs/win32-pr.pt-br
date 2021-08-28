---
title: Variáveis de Estado de Transformação
description: Variáveis de Estado de Transformação
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variáveis de estado de transformação OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c79b4363419d97a64184dd2408a9f6221ada52adc49adbb28eb3d049a4b2a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011914"
---
# <a name="transformation-state-variables"></a>Variáveis de Estado de Transformação

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>MATRIZ GL \_ MODELVIEW \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Pilha de matriz do Modelview             |
| Grupo de atributos: |                                    |
| Valor inicial:   | Identidade                           |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>MATRIZ \_ DE PROJEÇÃO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Pilha de matriz de projeção                                                        |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | Identidade                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>MATRIZ \_ DE TEXTURA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Pilha de matriz de textura                                                           |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | Identidade                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL \_ VIEWPORT</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Origem e extensão do viewport                                                       |
| Grupo de atributos: | Viewport                                                                         |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>INTERVALO \_ DE PROFUNDIDADE \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Intervalo de profundidade próximo e distante                                                       |
| Grupo de atributos: | Viewport                                                                       |
| Valor inicial:   | 0, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL \_ MODELVIEW \_ STACK \_ DEPTH</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ponteiro de pilha de matriz do Modelview                                                   |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>PROFUNDIDADE DA \_ PILHA \_ DE PROJEÇÃO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ponteiro de pilha da matriz de projeção                                                  |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>PROFUNDIDADE \_ DA PILHA DE TEXTURA \_ \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ponteiro de pilha da matriz de textura                                                     |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>MODO DE \_ MATRIZ \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Modo de matriz atual                                                              |
| Grupo de atributos: | transformação                                                                        |
| Valor inicial:   | GL \_ MODELVIEW                                                                    |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ NORMALIZE</dt> <dd> 

| Propriedade | Valor |
|------------------|-------------------------------------|
| Descrição:     | Ativar/desativar normalização normal atual |
| Grupo de atributos: | transformar/habilitar                    |
| Valor inicial:   | GL \_ falso                           |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>Recorte de \_ \_ plano GL *i*</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------|
| Descrição:     | Coeficientes de plano de recorte do usuário         |
| Grupo de atributos: | transformação                                |
| Valor inicial:   | 0, 0, 0, 0                               |
| Comando Get:     | [**glGetClipPlane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>Recorte de \_ \_ plano GL *i*</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     |  plano de recorte de usuário habilitado |
| Grupo de atributos: | transformar/habilitar                   |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> </dl>

 

 




