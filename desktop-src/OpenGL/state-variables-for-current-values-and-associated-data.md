---
title: Variáveis de Estado para Valores Atuais e Dados Associados
description: Variáveis de Estado para Valores Atuais e Dados Associados
ms.assetid: 8e47b119-a065-43c5-b7f5-76deaf975ad8
keywords:
- Variáveis de estado para valores atuais e openGL de dados associados
topic_type:
- apiref
api_name:
- State Variables for Current Values and Associated Data
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d99a9504a673d23d6923d5faf0e99770f20fe55e1cdd6b63d9adcbe68282584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553706"
---
# <a name="state-variables-for-current-values-and-associated-data"></a>Variáveis de Estado para Valores Atuais e Dados Associados

<dl> <dt><span id="GL_CURRENT_COLOR"></span><span id="gl_current_color"></span>COR \_ ATUAL DO \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------|
| Descrição:     | Cor atual                                                                                                        |
| Grupo de atributos: | atual                                                                                                              |
| Valor inicial:   | 1, 1, 1, 1                                                                                                           |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_INDEX"></span><span id="gl_current_index"></span>GL \_ CURRENT \_ INDEX</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição:     | Índice de cores atual                                                                                                                                            |
| Grupo de atributos: | atual                                                                                                                                                        |
| Valor inicial:   | 1                                                                                                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_TEXTURE_COORDS"></span><span id="gl_current_texture_coords"></span>\_COORDS DE TEXTURA ATUAL \_ \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Coordenadas de textura atuais                                                    |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_NORMAL"></span><span id="gl_current_normal"></span>GL \_ CURRENT \_ NORMAL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Normal atual                                                                 |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0, 0, 1                                                                        |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION"></span><span id="gl_current_raster_position"></span>POSIÇÃO \_ DE \_ RASTER ATUAL DO GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Posição atual do raster                                                        |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_DISTANCE"></span><span id="gl_current_raster_distance"></span>DISTÂNCIA \_ DE \_ RASTER ATUAL \_ DO GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Distância atual do raster                                                        |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_COLOR"></span><span id="gl_current_raster_color"></span>COR \_ DO \_ RASTER ATUAL DO GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição:     | Cor associada à posição de raster                                                                                                                          |
| Grupo de atributos: | atual                                                                                                                                                        |
| Valor inicial:   | 1, 1, 1, 1                                                                                                                                                     |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_INDEX"></span><span id="gl_current_raster_index"></span>GL \_ CURRENT \_ RASTER \_ INDEX</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição:     | Índice de cores associado à posição de raster                                                                                                                    |
| Grupo de atributos: | atual                                                                                                                                                        |
| Valor inicial:   | 1                                                                                                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_TEXTURE_COORDS"></span><span id="gl_current_raster_texture_coords"></span>\_COORDS DE TEXTURA DE \_ RASTER \_ ATUAL \_ GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Coordenadas de textura associadas à posição de raster                            |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION_VALID"></span><span id="gl_current_raster_position_valid"></span>POSIÇÃO \_ DE \_ RASTER ATUAL GL \_ \_ VÁLIDA</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Bit válido da posição de raster                                                        |
| Grupo de atributos: | atual                                                                          |
| Valor inicial:   | GL \_ TRUE                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_EDGE_FLAG"></span><span id="gl_edge_flag"></span>SINALIZADOR GL \_ EDGE \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Sinalizador de borda                                                                        |
| Grupo de atributos: | atual                                                                          |
| Valor inicial:   | GL \_ TRUE                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




