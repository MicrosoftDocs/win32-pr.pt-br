---
title: Variáveis de Estado de Rasterização
description: Variáveis de Estado de Rasterização
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
ms.openlocfilehash: 1586861eee26f93bca85b8c0f03e9f746e983046bbda755b67a792d65d660b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776886"
---
# <a name="rasterization-state-variables"></a>Variáveis de Estado de Rasterização

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>TAMANHO \_ DO PONTO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Tamanho do ponto                         |
| Grupo de atributos: | point                              |
| Valor inicial:   | 1.0                                |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL \_ POINT \_ SMOOTH</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Alias de ponto em                  |
| Grupo de atributos: | point/enable                       |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>LARGURA \_ DA LINHA \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Largura da linha                                                                     |
| Grupo de atributos: | line                                                                           |
| Valor inicial:   | 1.0                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL \_ LINE \_ SMOOTH</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Antialiação de linha em               |
| Grupo de atributos: | linha/habilitar                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>PADRÃO GL \_ \_ LINEPPLE \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Linepple                                                                     |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL \_ \_ LINEPPLE \_ REPEAT</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Repetição da apple de linha                                                              |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>GL \_ \_ LINEPPLE</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Habilitar a apple de linha                |
| Grupo de atributos: | linha/habilitar                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>ROSTO \_ DE REDUÇÃO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Eliminação de polígono habilitada            |
| Grupo de atributos: | polígono/habilitar                     |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>MODO \_ DE FACE DE REDUÇÃO \_ \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Retração de polígonos voltados para a frente/para trás                                           |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | GL \_ regressivo                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>\_frontal \_ face do GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Indicador de PV frontal/CCW do polígono                                              |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | \_CCW GL                                                                          |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>\_suavização do polígono GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Anti-aliasing em polígono em            |
| Grupo de atributos: | polígono/habilitar                     |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>\_modo de polígono GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Modo de rasterização de polígono (frente e verso)                                      |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | preenchimento do GL \_                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>polígono do GL \_ \_ STIPPLE</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Habilitar Stipple de polígono             |
| Grupo de atributos: | polígono/habilitar                     |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 



| Propriedade | Valor |
|------------------|----------------------------------------------------|
| Descrição:     | Padrão Stipple de polígono                            |
| Grupo de atributos: | polígono-Stipple                                    |
| Valor inicial:   | 1 ' s                                                |
| Comando Get:     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




