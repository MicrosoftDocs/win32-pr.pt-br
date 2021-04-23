---
title: Variáveis de estado para valores atuais e dados associados
description: Variáveis de estado para valores atuais e dados associados
ms.assetid: 8e47b119-a065-43c5-b7f5-76deaf975ad8
keywords:
- Variáveis de estado para valores atuais e dados associados OpenGL
topic_type:
- apiref
api_name:
- State Variables for Current Values and Associated Data
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 149139bc11698469ce0667c2ecf77bc7ab239adb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908464"
---
# <a name="state-variables-for-current-values-and-associated-data"></a>Variáveis de estado para valores atuais e dados associados

<dl> <dt><span id="GL_CURRENT_COLOR"></span><span id="gl_current_color"></span>a \_ cor atual do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------|
| Descrição:     | Cor atual                                                                                                        |
| Grupo de atributos: | atual                                                                                                              |
| Valor inicial:   | 1, 1, 1, 1                                                                                                           |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_INDEX"></span><span id="gl_current_index"></span>\_índice atual do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição:     | Índice de cores atual                                                                                                                                            |
| Grupo de atributos: | atual                                                                                                                                                        |
| Valor inicial:   | 1                                                                                                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_TEXTURE_COORDS"></span><span id="gl_current_texture_coords"></span>GL \_ \_ CoOrds de textura atual \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Coordenadas de textura atuais                                                    |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_NORMAL"></span><span id="gl_current_normal"></span>GL \_ \_ normal atual</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Normal atual                                                                 |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0, 0, 1                                                                        |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION"></span><span id="gl_current_raster_position"></span>\_posição de \_ rasterização atual do GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Posição de rasterização atual                                                        |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_DISTANCE"></span><span id="gl_current_raster_distance"></span>\_distância de \_ rasterização atual GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Distância de rasterização atual                                                        |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_COLOR"></span><span id="gl_current_raster_color"></span>a \_ \_ cor de rasterização atual do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição:     | Cor associada à posição da rasterização                                                                                                                          |
| Grupo de atributos: | atual                                                                                                                                                        |
| Valor inicial:   | 1, 1, 1, 1                                                                                                                                                     |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_INDEX"></span><span id="gl_current_raster_index"></span>\_índice de \_ varredura \_ atual do GL</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrição:     | Índice de cores associado à posição da rasterização                                                                                                                    |
| Grupo de atributos: | atual                                                                                                                                                        |
| Valor inicial:   | 1                                                                                                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_TEXTURE_COORDS"></span><span id="gl_current_raster_texture_coords"></span>GL \_ \_ CoOrds de textura de rasterização atual \_ \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Coordenadas de textura associadas à posição de rasterização                            |
| Grupo de atributos: | atual                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION_VALID"></span><span id="gl_current_raster_position_valid"></span>GL \_ atual \_ posição de rasterização \_ \_ válida</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Bit válido da posição de varredura                                                        |
| Grupo de atributos: | atual                                                                          |
| Valor inicial:   | GL \_ verdadeiro                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_EDGE_FLAG"></span><span id="gl_edge_flag"></span>sinalizador do GL \_ Edge \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Sinalizador de borda                                                                        |
| Grupo de atributos: | atual                                                                          |
| Valor inicial:   | GL \_ verdadeiro                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




