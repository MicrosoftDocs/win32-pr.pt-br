---
title: Variáveis de estado de iluminação
description: Variáveis de estado de iluminação
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Variáveis de estado de iluminação OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5a2d029727f4ff4a9eee353230e0843a39f082
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909844"
---
# <a name="lighting-state-variables"></a>Variáveis de estado de iluminação

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>\_iluminação GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | True se a iluminação estiver habilitada        |
| Grupo de atributos: | iluminação/habilitação                    |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_material de cor GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | True se o controle de cores estiver habilitado  |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_parâmetro de \_ material de cor GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Propriedades do material rastreando a cor atual                                       |
| Grupo de atributos: | iluminação                                                                         |
| Valor inicial:   | \_ambiente GL \_ e \_ difuso                                                        |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_material de cor GL \_ \_ face</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Rostos afetadas pelo controle de cores                                                 |
| Grupo de atributos: | iluminação                                                                         |
| Valor inicial:   | GL \_ frontal \_ e \_ posterior                                                             |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_ambiente GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------|
| Descrição:     | Cor do material de ambiente                   |
| Grupo de atributos: | iluminação                                 |
| Valor inicial:   | (0.2, 0.2, 0.2, 1,0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_difusão GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------|
| Descrição:     | Cor do material difuso                   |
| Grupo de atributos: | iluminação                                 |
| Valor inicial:   | (0,8, 0,8, 0,8, 1,0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_ESPECULA GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------|
| Descrição:     | Cor do material especular                  |
| Grupo de atributos: | iluminação                                 |
| Valor inicial:   | (0,0, 0,0, 0,0, 1,0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_emissão GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------|
| Descrição:     | Cor do material de emissiva                  |
| Grupo de atributos: | iluminação                                 |
| Valor inicial:   | (0,0, 0,0, 0,0, 1,0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>claridade do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------------|
| Descrição:     | Expoente de material especular            |
| Grupo de atributos: | iluminação                                 |
| Valor inicial:   | 0.0                                      |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>\_ambiente de \_ modelo \_ Light GL</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | Cor da cena ambiente                                                            |
| Grupo de atributos: | iluminação                                                                       |
| Valor inicial:   | (0.2, 0.2, 0.2, 1,0)                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ Visualizador local de modelo Light \_ GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | O visualizador é local                                                                  |
| Grupo de atributos: | iluminação                                                                         |
| Valor inicial:   | GL \_ falso                                                                        |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>\_Método Light \_ GL \_ dois \_ lados</dt> <dd> 

| Propriedade | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Usar iluminação de dois lados                                                           |
| Grupo de atributos: | iluminação                                                                         |
| Valor inicial:   | GL \_ falso                                                                        |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_ambiente GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Intensidade de ambiente da *leve*     |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | (0,0, 0,0, 0,0, 1,0)                  |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_difusão GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Intensidade difusa da luz *i*     |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   |                                    |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_ESPECULA GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Intensidade especular da luz *i*    |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   |                                    |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>\_posição GL</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Posição da luz *i*              |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | (0,0, 0,0, 1,0, 0,0)                  |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_atenuação de constante GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Fator de atenuação constante        |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | 1.0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_atenuação linear do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Fator de atenuação linear          |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | 0.0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_atenuação quadrática do GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Fator de atenuação quadrática       |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | 0.0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>\_direção de spot GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Direção do destaque da luz *i*   |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | (0,0, 0,0,-1,0)                     |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>\_expoente de spot de GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Expoente de destaque da luz *i*    |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | 0.0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>\_corte de spot GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | Ângulo de destaque da leve *i*       |
| Grupo de atributos: | iluminação                           |
| Valor inicial:   | 180,0                              |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ claro *i*</dt> <dd> 

| Propriedade | Valor |
|------------------|------------------------------------|
| Descrição:     | True se o Light *i* estiver habilitado          |
| Grupo de atributos: | iluminação/habilitação                    |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>\_índices de cores GL \_</dt> <dd> 

| Propriedade | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descrição:     | *C (a)*, *c (d)* e *c (s)* para a iluminação de índice de cor                         |
| Grupo de atributos: | iluminação/habilitação                                                                |
| Valor inicial:   | 0, 1, 1                                                                          |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




