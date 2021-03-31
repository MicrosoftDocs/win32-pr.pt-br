---
title: Variáveis de estado de controle framebuffer
description: Variáveis de estado de controle framebuffer
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
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823096"
---
# <a name="framebuffer-control-state-variables"></a>Variáveis de estado de controle framebuffer

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_buffer de desenho GL \_</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| Descrição:     | Buffers selecionados para desenho           |
| Grupo de atributos: | buffer de cores                           |
| Valor inicial:   |                                        |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_WRITEMASK de índice GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Writemask de índice de cores                                                            |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | 1 ' s                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK de cores GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Habilitação de gravação de cores; R, G, B ou A                                               |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | GL \_ verdadeiro                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_WRITEMASK de profundidade GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Buffer de profundidade habilitado para gravação                                                 |
| Grupo de atributos: | profundidade-buffer                                                                     |
| Valor inicial:   | GL \_ verdadeiro                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_WRITEMASK de estêncil GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Writemask de buffer de estêncil                                                         |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | 1 ' s                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_valor de \_ limpeza de cor GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Valor de limpeza do buffer de cores (modo RGBA)                                           |
| Grupo de atributos: | buffer de cores                                                                   |
| Valor inicial:   | 0, 0, 0, 0                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_valor de \_ limpeza de índice GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Valor de limpeza do buffer de cores (modo de índice de cor)                                    |
| Grupo de atributos: | buffer de cores                                                                   |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_valor de \_ limpeza de profundidade GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Profundidade-valor de limpeza do buffer                                                         |
| Grupo de atributos: | profundidade-buffer                                                                     |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_valor de \_ limpeza do estêncil GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Estêncil-valor de limpeza do buffer                                                       |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>valor de limpeza do GL \_ Accum \_ \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Acumulação-valor de limpeza do buffer                                                |
| Grupo de atributos: | Accum-buffer                                                                   |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




