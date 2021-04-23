---
title: Variáveis de estado de transformação
description: Variáveis de estado de transformação
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
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908824"
---
# <a name="transformation-state-variables"></a>Variáveis de estado de transformação

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_MODELVIEW \_ matriz GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Pilha de matriz Modelview             |
| Grupo de atributos: |                                    |
| Valor inicial:   | Identidade                           |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matriz de projeção GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Pilha de matriz de projeção                                                        |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | Identidade                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matriz de textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Pilha de matriz de textura                                                           |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | Identidade                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_visor GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Origem e extensão do visor                                                       |
| Grupo de atributos: | visor                                                                         |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_intervalo de profundidade do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Intervalo de profundidade próximo e longe                                                       |
| Grupo de atributos: | visor                                                                       |
| Valor inicial:   | 0, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>\_profundidade de \_ pilha \_ MODELVIEW GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ponteiro de pilha de matriz Modelview                                                   |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_profundidade da pilha de projeção GL \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ponteiro da pilha da matriz de projeção                                                  |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>\_profundidade da \_ pilha de textura GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ponteiro de pilha da matriz de textura                                                     |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_modo de matriz GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Modo de matriz atual                                                              |
| Grupo de atributos: | transformação                                                                        |
| Valor inicial:   | \_MODELVIEW GL                                                                    |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>\_NORMALIZE GL</dt> <dd> 

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

 

 




