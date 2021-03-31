---
title: Variáveis de estado de rasterização
description: Variáveis de estado de rasterização
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- Variáveis de estado de rasterização OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1667c530ea1db8c9e463be0edad5de98e8b107
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638568"
---
# <a name="rasterization-state-variables"></a>Variáveis de estado de rasterização

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>\_tamanho do ponto GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Tamanho do ponto                         |
| Grupo de atributos: | point                              |
| Valor inicial:   | 1,0                                |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>\_simples ponto \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Alias de ponto em                  |
| Grupo de atributos: | ponto/ativação                       |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>\_largura da linha gl \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Largura da linha                                                                     |
| Grupo de atributos: | line                                                                           |
| Valor inicial:   | 1,0                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>linha do GL \_ \_ Smooth</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Suavização de linha em               |
| Grupo de atributos: | linha/habilitar                        |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>\_padrão de \_ STIPPLE de linha gl \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Stipple de linha                                                                     |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1 ' s                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>\_STIPPLE de linha gl \_ \_ repetir</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Repetir Stipple de linha                                                              |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>\_STIPPLE de linha gl \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Habilitar Stipple de linha                |
| Grupo de atributos: | linha/habilitar                        |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>\_face de seleção GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Remoção de polígono habilitada            |
| Grupo de atributos: | polígono/habilitar                     |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>\_modo de seleção de \_ face GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Selecionar polígonos front-face/verso                                           |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | GL \_ regressivo                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>\_frontal \_ face do GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Indicador de PV frontal/CCW do polígono                                              |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | \_CCW GL                                                                          |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>\_suavização do polígono GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Anti-aliasing em polígono em            |
| Grupo de atributos: | polígono/habilitar                     |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>\_modo de polígono GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Modo de rasterização de polígono (frente e verso)                                      |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | preenchimento do GL \_                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>polígono do GL \_ \_ STIPPLE</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Habilitar Stipple de polígono             |
| Grupo de atributos: | polígono/habilitar                     |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 



|                  |                                                    |
|------------------|----------------------------------------------------|
| Descrição:     | Padrão Stipple de polígono                            |
| Grupo de atributos: | polígono-Stipple                                    |
| Valor inicial:   | 1 ' s                                                |
| Comando Get:     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




