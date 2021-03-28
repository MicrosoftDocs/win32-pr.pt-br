---
title: Constantes D3DCOMPILE (D3DCompiler. h)
description: As constantes D3DCOMPILE especificam como o compilador compila o código HLSL.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172941"
---
# <a name="d3dcompile-constants"></a>Constantes D3DCOMPILE

As constantes D3DCOMPILE especificam como o compilador compila o código HLSL.

<dl> <dt>

<span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**\_Depuração D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Direciona o compilador para inserir informações de arquivo/linha/tipo/símbolo de depuração no código de saída.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ ignorar \_ validação**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Instrui o compilador a não validar o código gerado em relação a recursos e restrições conhecidos. É recomendável que você use essa constante apenas com sombreadores que foram compilados com êxito no passado. O DirectX sempre valida os sombreadores antes de defini-los para um dispositivo.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ ignorar \_ otimização**
</dt> <dd> <dl> <dt>

(1 << 2)
</dt> <dt>



Direciona o compilador para ignorar as etapas de otimização durante a geração de código. É recomendável que você defina essa constante somente para fins de depuração.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**Linha de matriz do pacote de D3DCOMPILE \_ \_ \_ \_ principal**
</dt> <dd> <dl> <dt>

(1 << 3)
</dt> <dt>



Direciona o compilador para pacotes de matrizes em ordem de linha principal na entrada e na saída do sombreador.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**\_Coluna de matriz de pacote D3DCOMPILE \_ \_ \_ principal**
</dt> <dd> <dl> <dt>

(1 << 4)
</dt> <dt>



Direciona o compilador para pacotes de matrizes na ordem principal da coluna na entrada e na saída do sombreador. Esse tipo de empacotamento é geralmente mais eficiente, pois uma série de produtos de ponto pode executar a multiplicação de matriz de vetor.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Precisão parcial do D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 5)
</dt> <dt>



Direciona o compilador para executar todos os cálculos com precisão parcial. Se você definir essa constante, o código compilado poderá ser executado mais rapidamente em algum hardware.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ Force \_ vs \_ software \_ sem \_ aceitar**
</dt> <dd> <dl> <dt>

(1 << 6)
</dt> <dt>



Direciona o compilador para compilar um sombreador de vértice para o próximo perfil de sombreador mais alto. Essa constante ativa a depuração e otimizações.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ forçar \_ o \_ software PS \_ não \_ aceitar**
</dt> <dd> <dl> <dt>

(1 << 7)
</dt> <dt>



Direciona o compilador para compilar um sombreador de pixel para o próximo perfil de sombreador mais alto. Essa constante também ativa a depuração e otimizações.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ sem \_ preshadr**
</dt> <dd> <dl> <dt>

(1 << 8)
</dt> <dt>



Direciona o compilador para desabilitar os preshaders. Se você definir essa constante, o compilador não extrairá a expressão estática para avaliação.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ evitar \_ controle de fluxo \_**
</dt> <dd> <dl> <dt>

(1 << 9)
</dt> <dt>



Instrui o compilador a não usar construções de controle de fluxo sempre que possível.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ prefiro \_ o \_ controle de fluxo**
</dt> <dd> <dl> <dt>

(1 << 10)
</dt> <dt>



Instrui o compilador a usar construções de controle de fluxo sempre que possível.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ habilitar \_ restrição**
</dt> <dd> <dl> <dt>

(1 << 11)
</dt> <dt>



Força a compilação estrita, que pode não permitir a sintaxe herdada.

Por padrão, o compilador desabilita a restrição na sintaxe preterida.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ habilitar a \_ compatibilidade com versões anteriores \_**
</dt> <dd> <dl> <dt>

(1 << 12)
</dt> <dt>



Direciona o compilador para permitir que os sombreadores mais antigos sejam compilados em destinos de 5 \_ 0.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ Strict**
</dt> <dd> <dl> <dt>

(1 << 13)
</dt> <dt>



Força a compilação IEEE estrita.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE \_ otimização \_ LEVEL0**
</dt> <dd> <dl> <dt>

(1 << 14)
</dt> <dt>



Direciona o compilador para usar o nível de otimização mais baixo. Se você definir essa constante, o compilador poderá produzir um código mais lento, mas produzirá o código mais rapidamente. Defina essa constante ao desenvolver o sombreador iterativamente.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ otimização \_ LEVEL1**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Direciona o compilador para usar o segundo nível de otimização mais baixo.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE \_ otimização \_ LEVEL2**
</dt> <dd> <dl> <dt>

((1 << 14) \| (1 << 15))
</dt> <dt>



Direciona o compilador para usar o segundo nível de otimização mais alto.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE \_ otimização \_ LEVEL3**
</dt> <dd> <dl> <dt>

(1 << 15)
</dt> <dt>



Direciona o compilador para usar o nível de otimização mais alto. Se você definir essa constante, o compilador produzirá o melhor código possível, mas poderá levar muito mais tempo para fazer isso. Defina essa constante para as compilações finais de um aplicativo quando o desempenho for o fator mais importante.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**\_Avisos D3DCOMPILE \_ são \_ erros**
</dt> <dd> <dl> <dt>

(1 << 18)
</dt> <dt>



Direciona o compilador para tratar todos os avisos como erros ao compilar o código do sombreador. Recomendamos que você use essa constante para o novo código de sombreador, para que você possa resolver todos os avisos e reduzir o número de defeitos de código difíceis de encontrar.


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE de \_ recursos \_ podem \_ alias**
</dt> <dd> <dl> <dt>

(1 << 19)
</dt> <dt>



Direciona o compilador para pressupor que os modos de exibição de acesso não ordenados (UAVs) e do Shader Resource views (SRVs) podem ser alias para cs \_ 5 \_ 0.

> [!Note]  
> Essa constante do compilador é nova começando com o \_47.dll D3dcompiler.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ habilitar \_ \_ tabelas de DESCRITOr não associado \_**
</dt> <dd> <dl> <dt>

(1 << 20)
</dt> <dt>



Direciona o compilador para habilitar tabelas de descritor não associadas.

> [!Note]  
> Essa constante do compilador é nova começando com o \_47.dll D3dcompiler.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ todos os \_ recursos \_ associados**
</dt> <dd> <dl> <dt>

(1 << 21)
</dt> <dt>



Direciona o compilador para garantir que todos os recursos estejam associados.

> [!Note]  
> Essa constante do compilador é nova começando com o \_47.dll D3dcompiler.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





