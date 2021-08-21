---
title: Variáveis de Estado de Controle Framebuffer
description: Variáveis de Estado de Controle Framebuffer
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variáveis de estado de controle framebuffer OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 276019f790e5f4750e446cf4ae2d035e0178d0e79130100a5a5e1954cbdcb73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061905"
---
# <a name="framebuffer-control-state-variables"></a>Variáveis de Estado de Controle Framebuffer

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_buffer de desenho GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------|
| Descrição:     | Buffers selecionados para desenho           |
| Grupo de atributos: | buffer de cores                           |
| Valor inicial:   |                                        |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_WRITEMASK de índice GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Writemask de índice de cores                                                            |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | 1 ' s                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK de cores GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Habilitação de gravação de cores; R, G, B ou A                                               |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | GL \_ verdadeiro                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_WRITEMASK de profundidade GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Buffer de profundidade habilitado para gravação                                                 |
| Grupo de atributos: | profundidade-buffer                                                                     |
| Valor inicial:   | GL \_ verdadeiro                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_WRITEMASK de estêncil GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Writemask de buffer de estêncil                                                         |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | 1 ' s                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_valor de \_ limpeza de cor GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Valor de limpeza do buffer de cores (modo RGBA)                                           |
| Grupo de atributos: | buffer de cores                                                                   |
| Valor inicial:   | 0, 0, 0, 0                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_valor de \_ limpeza de índice GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Valor de limpeza do buffer de cores (modo de índice de cor)                                    |
| Grupo de atributos: | buffer de cores                                                                   |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_valor de \_ limpeza de profundidade GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade-valor de limpeza do buffer                                                         |
| Grupo de atributos: | profundidade-buffer                                                                     |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_valor de \_ limpeza do estêncil GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Estêncil-valor de limpeza do buffer                                                       |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>VALOR \_ CLARO DE GL \_ \_ ACCUM</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Valor desem buffer de acúmulo                                                |
| Grupo de atributos: | accum-buffer                                                                   |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




