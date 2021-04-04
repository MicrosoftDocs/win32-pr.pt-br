---
title: Operações de pixel
description: Operações de pixel
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Operações de pixel OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823197"
---
# <a name="pixel-operations"></a>Operações de pixel

<dl> <dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_teste de tesoura do GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Recorte habilitado                 |
| Grupo de atributos: | recorte/habilitação                     |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_caixa de tesoura GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Caixa de tesoura                                                                      |
| Grupo de atributos: | tesoura                                                                          |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_teste de estêncil GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Estêncil habilitado                 |
| Grupo de atributos: | estêncil-buffer/habilitar              |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>o \_ estêncil GL \_ Func</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Função de estêncil                                                                 |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | GL \_ sempre                                                                       |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_máscara de \_ valor de estêncil GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Máscara de estêncil                                                                     |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | 1 ' s                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_referência de estêncil GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Valor de referência do estêncil                                                          |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_falha no estêncil GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ação de falha de estêncil                                                              |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | \_Keep GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>\_falha de \_ profundidade de aprovação do estêncil GL \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ação falha no buffer de profundidade do estêncil                                                 |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | \_Keep GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_passo de \_ profundidade de passagem do estêncil GL \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Ação de passagem do buffer de profundidade do estêncil                                                 |
| Grupo de atributos: | estêncil-buffer                                                                   |
| Valor inicial:   | \_Keep GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>\_teste de alfa do GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Teste alfa habilitado                 |
| Grupo de atributos: | buffer de cores/habilitar                |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>razão de teste do GL \_ alfa \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Função de teste alfa                                                              |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | GL \_ sempre                                                                       |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>\_referência de \_ teste \_ alfa do GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Valor de referência de teste alfa                                                       |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_teste de profundidade GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Buffer de profundidade habilitado               |
| Grupo de atributos: | profundidade/buffer/habilitar                |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>\_funcm de profundidade do GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Função de teste do buffer de profundidade                                                       |
| Grupo de atributos: | profundidade-buffer                                                                     |
| Valor inicial:   | GL \_ menos                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>a \_ combinação GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Mesclagem habilitada                   |
| Grupo de atributos: | buffer de cores/habilitar                |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_origem GL BLENC \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Função de origem de mesclagem                                                         |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | GL \_ um                                                                          |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>\_hora de \_ verão do GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Função de destino de mesclagem                                                    |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | GL \_ zero                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_pontilhamento GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Pontilhamento habilitado                  |
| Grupo de atributos: | buffer de cores/habilitar                |
| Valor inicial:   | GL \_ verdadeiro                           |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_op lógico \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrição:     | Operação lógica habilitada          |
| Grupo de atributos: | buffer de cores/habilitar                |
| Valor inicial:   | GL \_ falso                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_modo de \_ op \_ lógico GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrição:     | Função de operação lógica                                                       |
| Grupo de atributos: | buffer de cores                                                                     |
| Valor inicial:   | \_cópia GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




