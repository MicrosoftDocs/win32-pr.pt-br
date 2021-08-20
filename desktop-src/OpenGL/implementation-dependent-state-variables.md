---
title: Variáveis de Estado Dependentes de Implementação
description: Variáveis de Estado Dependentes de Implementação
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Implementation-Dependent openGL de variáveis de estado
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da38f841408bd6ddf481473837f36544d21d896f2764317957c65158be27fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061454"
---
# <a name="implementation-dependent-state-variables"></a>Variáveis de Estado Dependentes de Implementação

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL \_ MAX \_ LIGHTS</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------|
| Descrição:     | Número máximo de luzes               |
| Grupo de atributos: |                                        |
| Valor inicial:   | 8                                      |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>PLANOS DE CLIPE GL \_ MAX \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Número máximo de planos de recorte do usuário                                           |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 6                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL \_ MAX \_ MODELVIEW \_ STACK \_ DEPTH</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha modelview-matrix                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>PROFUNDIDADE DA \_ PILHA \_ DE PROJEÇÃO \_ GL MAX \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha da matriz de projeção                                            |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>PROFUNDIDADE DA \_ PILHA DE TEXTURA GL MAX \_ \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha de matriz de textura                                            |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>GL \_ SUBPIXEL \_ BITS</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Número de bits de precisão de subpixel em *x* e *y*                              |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 4                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>TAMANHO \_ MÁXIMO \_ DA TEXTURA GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Altura máxima ou largura de uma imagem de textura (sem bordas)                     |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>TABELA DE \_ \_ MAPA DE PIXELS \_ GL MAX \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Tamanho máximo de uma **tabela de tradução glPixelMap**                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>PROFUNDIDADE DA \_ PILHA \_ DE NOMES \_ DE \_ GL MAX</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha de nomes de seleção                                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>\_ANINHAMENTO DE LISTA GL MAX \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Aninhamento máximo de chamada da lista de exibição                                                |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL \_ MAX \_ EVAL \_ ORDER</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ordem polinomial máxima do avaliador                                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 8                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL \_ MAX \_ VIEWPORT \_ DIMS</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Dimensões máximas do viewport                                                      |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL \_ MAX \_ ATTRIB \_ STACK \_ DEPTH</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha de atributos                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 16                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL \_ AUX \_ BUFFERS</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Número de buffers auxiliares                                                      |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>MODO \_ GL \_ RGBA</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | True se os buffers de cores armazenam RGBA                                                 |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>MODO GL \_ INDEX \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | True se os buffers de cores armazenam índices                                              |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ DOUBLEBUFFER</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | True se existirem buffers front e back                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL \_ ESTÉREO</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | True se existirem buffers à esquerda e à direita                                           |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>INTERVALO \_ DE TAMANHO DO PONTO \_ \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Intervalo (de baixo a alto) de tamanhos de pontos antialiados                                 |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>\_GRANULARIDADE DO \_ TAMANHO DO PONTO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Granularidade do tamanho do ponto antialiased                                             |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>INTERVALO DE \_ LARGURA \_ DE LINHA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Intervalo (baixo para alto) de larguras de linha AntiAlias                                 |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>\_granularidade da \_ largura da linha gl \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Granularidade de largura de linha AntiAlias                                             |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




