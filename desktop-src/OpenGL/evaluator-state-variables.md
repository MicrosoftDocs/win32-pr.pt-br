---
title: Variáveis de Estado do Avaliador
description: Variáveis de Estado do Avaliador
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
ms.openlocfilehash: 747ed7c19817757570d6517c68a987c2c75aa340c74ecfbac9fe258b1091f00e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082506"
---
# <a name="evaluator-state-variables"></a>Variáveis de Estado do Avaliador

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL \_ ORDER</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | Ordem do mapa 1D                  |
| Grupo de atributos: |                                |
| Valor inicial:   | 1                              |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL \_ ORDER</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | Pedidos de mapa 2D                 |
| Grupo de atributos: |                                |
| Valor inicial:   | 1,1                            |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | Pontos de controle 1D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | Pontos de controle 2D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>DOMÍNIO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | Pontos de extremidade de domínio 1D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>DOMÍNIO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------|
| Descrição:     | Pontos de extremidade de domínio 2D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ MAP1 \_ x</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | O mapa 1D habilita: *x* é tipo de mapa   |
| Grupo de atributos: | eval/enable                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ MAP2 \_ x</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | O mapa 2D habilita: *x* é tipo de mapa   |
| Grupo de atributos: | eval/enable                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>DOMÍNIO DE GRADE GL \_ MAP1 \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Pontos de extremidade de grade 1D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0,1                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>DOMÍNIO \_ DE GRADE GL MAP2 \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Pontos de extremidade de grade 2D                                                             |
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

 

 




