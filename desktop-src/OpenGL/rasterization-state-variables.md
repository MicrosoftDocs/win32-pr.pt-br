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
ms.openlocfilehash: 6210f93c23dc52f19f3e01ea01ebe8fc9d631c8c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909834"
---
# <a name="rasterization-state-variables"></a>Variáveis de estado de rasterização

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>\_tamanho do ponto GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Tamanho do ponto                         |
| Grupo de atributos: | point                              |
| Valor inicial:   | 1.0                                |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>\_simples ponto \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Alias de ponto em                  |
| Grupo de atributos: | ponto/ativação                       |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>\_largura da linha gl \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Largura da linha                                                                     |
| Grupo de atributos: | line                                                                           |
| Valor inicial:   | 1.0                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>linha do GL \_ \_ Smooth</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Suavização de linha em               |
| Grupo de atributos: | linha/habilitar                        |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>\_padrão de \_ STIPPLE de linha gl \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Stipple de linha                                                                     |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1 ' s                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>\_STIPPLE de linha gl \_ \_ repetir</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Repetir Stipple de linha                                                              |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>\_STIPPLE de linha gl \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Habilitar Stipple de linha                |
| Grupo de atributos: | linha/habilitar                        |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>\_face de seleção GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Remoção de polígono habilitada            |
| Grupo de atributos: | polígono/habilitar                     |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>\_modo de seleção de \_ face GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Selecionar polígonos front-face/verso                                           |
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

 

 




