---
title: Variáveis de estado de Implementation-Dependent
description: Variáveis de estado de Implementation-Dependent
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Variáveis de estado do Implementation-Dependent OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645702c9ea91f21d0e3bce5233b8014fd8f86859
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909874"
---
# <a name="implementation-dependent-state-variables"></a>Variáveis de estado de Implementation-Dependent

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>\_luzes máximas GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------|
| Descrição:     | Número máximo de luzes               |
| Grupo de atributos: |                                        |
| Valor inicial:   | 8                                      |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>\_máximo de \_ recortes do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Número máximo de planos de recorte do usuário                                           |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 6                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>\_profundidade máxima \_ de \_ pilha de MODELVIEW \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha modelview-matriz                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>\_profundidade máxima \_ da \_ pilha de projeção GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha de matrizes                                            |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>\_profundidade máxima \_ da \_ pilha de textura \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha de matriz de textura                                            |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>\_bits de SUBPIXEL GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Número de bits de precisão de subpixel em *x* e *y*                              |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 4                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>\_tamanho máximo de \_ textura \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Altura ou largura máxima de uma imagem de textura (sem bordas)                     |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>\_tabela do \_ mapa de pixels máx \_ . gl \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Tamanho máximo de uma tabela de tradução de **glPixelMap**                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>\_profundidade máxima \_ da \_ pilha de nome \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Máximo de seleção-profundidade da pilha de nome                                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>\_ \_ aninhamento máximo de lista do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Aninhamento máximo de chamada de lista de exibição                                                |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL \_ máx \_ . \_ ordem de avaliação</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ordem polinomial do avaliador máximo                                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 8                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL \_ máx. de \_ viewport \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Máximo de dimensões do visor                                                      |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>\_profundidade máxima \_ de \_ pilha de Atrib \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade máxima da pilha de atributos                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 16                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>\_buffers auxiliares GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Número de buffers auxiliares                                                      |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>\_modo RGBA do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | True se os buffers de cores armazenar RGBA                                                 |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>\_modo de índice GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | True se os buffers de cores armazenarem índices                                              |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>\_DOUBLEBUFFER GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | True se existirem buffers de frente e de trás                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>\_estéreo GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | True se existirem buffers esquerdo e direito                                           |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>\_intervalo de \_ tamanho do ponto GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Intervalo (baixo para alto) de tamanhos de ponto AntiAlias                                 |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>\_granularidade do \_ tamanho do ponto GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Granularidade de tamanho de ponto AntiAlias                                             |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>\_intervalo de \_ largura da linha gl \_</dt> <dd> 

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

 

 




