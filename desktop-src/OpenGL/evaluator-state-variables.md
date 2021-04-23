---
title: Variáveis de estado do avaliador
description: Variáveis de estado do avaliador
ms.assetid: e7d710be-de17-46a0-8ad8-0f65b943ece8
keywords:
- Variáveis de estado do avaliador OpenGL
topic_type:
- apiref
api_name:
- Evaluator State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2895f773721f7c900003cbaa0f070c277a0e260
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909254"
---
# <a name="evaluator-state-variables"></a>Variáveis de estado do avaliador

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>\_ordem GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | ordem de mapa de 1-D                  |
| Grupo de atributos: |                                |
| Valor inicial:   | 1                              |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>\_ordem GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | pedidos de mapa 2-D                 |
| Grupo de atributos: |                                |
| Valor inicial:   | 1, 1                            |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>\_COEFF GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | pontos de controle de 1-D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>\_COEFF GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | pontos de controle 2D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>\_domínio GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | pontos de extremidade de domínio 1-D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>\_domínio GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | pontos de extremidade de domínio 2D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ MAP1 \_ x</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | o mapa 1-D habilita: *x* é o tipo de mapa   |
| Grupo de atributos: | eval/habilitação                        |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ map2 \_ x</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | o mapa 2-D habilita: *x* é o tipo de mapa   |
| Grupo de atributos: | eval/habilitação                        |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>Domínio de grade do GL \_ MAP1 \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | pontos de extremidade de grade 1-D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0, 1                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>Domínio de grade do GL \_ map2 \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | pontos de extremidade de grade 2D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0, 1; 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>\_Segmentos de \_ grade GL MAP1 \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | divisões de grade 1-D                 |
| Grupo de atributos: | eval                               |
| Valor inicial:   | 1                                  |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>\_Segmentos de \_ grade GL MAP1 \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | segmentos de grade 2D                                                              |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>GL \_ automático \_ normal</dt> <dd> 

| Propriedade | Valor |
|------------------|---------------------------------------------|
| Descrição:     | True se a geração normal automática estiver habilitada |
| Grupo de atributos: | eval                                        |
| Valor inicial:   | GL \_ falso                                   |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




