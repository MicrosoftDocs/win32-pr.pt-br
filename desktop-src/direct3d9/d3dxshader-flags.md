---
description: Os sinalizadores D3DXSHADER são usados para análise, compilação ou montagem de sombreadores.
ms.assetid: 8558d0e9-d09f-4c62-bc89-6080f4e44ff8
title: Sinalizadores D3DXSHADER (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_PACKMATRIX_COLUMNMAJOR
- D3DXSHADER_PACKMATRIX_ROWMAJOR
- D3DXSHADER_AVOID_FLOW_CONTROL
- D3DXSHADER_DEBUG
- D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_IEEE_STRICTNESS
- D3DXSHADER_NO_PRESHADER
- D3DXSHADER_OPTIMIZATION_LEVEL0
- D3DXSHADER_OPTIMIZATION_LEVEL1
- D3DXSHADER_OPTIMIZATION_LEVEL2
- D3DXSHADER_OPTIMIZATION_LEVEL3
- D3DXSHADER_PARTIALPRECISION
- D3DXSHADER_PREFER_FLOW_CONTROL
- D3DXSHADER_SKIPOPTIMIZATION
- D3DXSHADER_SKIPVALIDATION
- D3DXSHADER_USE_LEGACY_D3DX9_31_DLL
- D3DXSHADER_DEBUG
- D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT
- D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT
- D3DXSHADER_SKIPVALIDATION
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 6f5d35f8c3bdf556e188c2cab8ff2684449b226f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105751921"
---
# <a name="d3dxshader-flags"></a>Sinalizadores de D3DXSHADER

Os sinalizadores **D3DXSHADER** são usados para análise, compilação ou montagem de sombreadores.

**Sinalizadores do analisador**

Os sinalizadores de tempo de análise são usados apenas pelo sistema de efeitos (antes da compilação de efeito) quando você cria um compilador de efeito. Por exemplo, você pode criar um objeto de compilador com **D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR** e, em seguida, usar esse objeto de compilador repetidamente com diferentes sinalizadores de compilador para gerar código especializado.



| Constante                                                                                                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_PACKMATRIX_COLUMNMAJOR"></span><span id="d3dxshader_packmatrix_columnmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX \_ COLUMNMAJOR**</dt> </dl> | A menos que especificado explicitamente, as matrizes serão empacotadas na ordem de coluna principal (cada vetor estará em uma única coluna) quando passar de e para o sombreador. Isso geralmente é mais eficiente, pois permite que a multiplicação de matriz de vetor seja executada usando uma série de produtos dot.<br/> |
| <span id="D3DXSHADER_PACKMATRIX_ROWMAJOR"></span><span id="d3dxshader_packmatrix_rowmajor"></span><dl> <dt>**D3DXSHADER \_ PACKMATRIX da \_ primária**</dt> </dl>          | A menos que especificado explicitamente, as matrizes serão empacotadas na ordem de linha principal (cada vetor estará em uma única linha) quando passado para ou do sombreador.<br/>                                                                                                                                        |



**Sinalizadores de compilador**

O compilador DirectX 10 HLSL agora é o compilador padrão. Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.

A tabela a seguir fornece detalhes dos sinalizadores disponíveis no Direct3D 9 e no Direct3D 10. O valor do sinalizador é a opção FXC equivalente.



| Constante/valor                                                                                                                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_AVOID_FLOW_CONTROL"></span><span id="d3dxshader_avoid_flow_control"></span><dl> <dt>**D3DXSHADER \_ EVITAR \_ \_**</dt> <dt>/GFA</dt> de controle de fluxo </dl>                                     | Essa é uma dica ao compilador para evitar o uso de instruções de controle de fluxo.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**D3DXSHADER \_ Depurar**</dt> <dt>/Zi</dt> </dl>                                                                               | Insira o nome de arquivo de depuração, números de linha e informações de tipo e símbolo durante a compilação do sombreador.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="D3DXSHADER_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dxshader_enable_backwards_compatibility"></span><dl> <dt>**D3DXSHADER \_ Habilitar/GEC de \_ \_ compatibilidade com versões anteriores**</dt> <dt></dt> </dl> | Compile \_ \_ os sombreadores PS 1 x como PS \_ 2 \_ 0. Os efeitos que especificam \_ destinos PS 1 \_ x serão compilados em \_ destinos PS 2 \_ 0 porque essa é a versão mínima do sombreador com suporte da versão do compilador do sombreador fornecida com o DirectX 10. Esse sinalizador não tem nenhum efeito quando usado com destinos de compilação de nível superior.<br/> Direct3D 9-não<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORÇAR \_ PS \_ software \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | Force o compilador a Compilar no próximo destino de software mais alto disponível para sombreadores de pixel. Esse sinalizador também desativa as otimizações e a depuração.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ FORÇAR \_ vs \_ software \_ NOOPT**</dt> <dt>N/A</dt> </dl>                      | Force o compilador a Compilar no próximo destino de software mais alto disponível para os sombreadores de vértice. Esse sinalizador também desativa as otimizações e a depuração.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_IEEE_STRICTNESS"></span><span id="d3dxshader_ieee_strictness"></span><dl> <dt>**D3DXSHADER \_ /GIS de \_ restrição IEEE**</dt> <dt></dt> </dl>                                               | Desabilite otimizações que podem fazer com que a saída de um programa de sombreador compilado difira da saída de um programa compilado com o compilador do sombreador DirectX 9 devido a erros de precisão pequena em matemática de ponto flutuante.<br/> Direct3D 9-não<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="D3DXSHADER_NO_PRESHADER"></span><span id="d3dxshader_no_preshader"></span><dl> <dt>**D3DXSHADER \_ SEM \_ /op PREshadr**</dt> <dt></dt> </dl>                                                         | Desabilita os preshaders. O compilador não efetuará pull de expressões estáticas para avaliação na CPU do host. Além disso, o compilador não loft nenhuma expressão ao compilar funções autônomas.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL0"></span><span id="d3dxshader_optimization_level0"></span><dl> <dt>**D3DXSHADER \_ OTIMIZAÇÃO \_ LEVEL0**</dt> <dt>/o0</dt> </dl>                                    | Nível de otimização mais baixo. Pode produzir um código mais lento, mas fará isso mais rapidamente. Isso pode ser útil em um ciclo de desenvolvimento de sombreador altamente iterativo.<br/> Direct3D 9-não<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL1"></span><span id="d3dxshader_optimization_level1"></span><dl> <dt>**D3DXSHADER \_ OTIMIZAÇÃO \_ LEVEL1**</dt> <dt>/O1</dt> </dl>                                    | Segundo nível de otimização mais baixo.<br/> Direct3D 9-não<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL2"></span><span id="d3dxshader_optimization_level2"></span><dl> <dt>**D3DXSHADER \_ OTIMIZAÇÃO \_ LEVEL2**</dt> <dt>/O2</dt> </dl>                                    | Segundo nível de otimização mais alto.<br/> Direct3D 9-não<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="D3DXSHADER_OPTIMIZATION_LEVEL3"></span><span id="d3dxshader_optimization_level3"></span><dl> <dt>**D3DXSHADER \_ OTIMIZAÇÃO \_ LEVEL3**</dt> <dt>/O3</dt> </dl>                                    | Nível de otimização mais alto. Produzirá o melhor código possível, mas pode levar muito mais tempo para fazer isso. Isso será útil para as compilações finais de um aplicativo em que o desempenho é o fator mais importante.<br/> Direct3D 9-não<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_PARTIALPRECISION"></span><span id="d3dxshader_partialprecision"></span><dl> <dt>**D3DXSHADER \_ PARTIALPRECISION**</dt> <dt>/GPP</dt> </dl>                                             | Forçar a ocorrência de todos os cálculos no sombreador resultante a uma precisão parcial. Isso pode resultar em uma avaliação mais rápida de sombreadores em algum hardware.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="D3DXSHADER_PREFER_FLOW_CONTROL"></span><span id="d3dxshader_prefer_flow_control"></span><dl> <dt>**D3DXSHADER \_ PREFERIR \_ \_**</dt> <dt>/GFP,</dt> de controle de fluxo </dl>                                  | Essa é uma dica ao compilador para preferir o uso de instruções de controle de fluxo.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DXSHADER_SKIPOPTIMIZATION"></span><span id="d3dxshader_skipoptimization"></span><dl> <dt>**D3DXSHADER \_ SKIPOPTIMIZATION**</dt> <dt>/OD</dt> </dl>                                              | Instrua o compilador a ignorar as etapas de otimização durante a geração de código. A menos que você esteja tentando isolar um problema em seu código e suspeitar do compilador, não é recomendável usar essa opção.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> <dt>/VD</dt> </dl>                                                    | Não valide o código gerado em relação a funcionalidades e restrições conhecidas. Essa opção é recomendada somente ao compilar sombreadores que são conhecidos como trabalho (ou seja, sombreadores que foram compilados antes sem essa opção). Os sombreadores sempre são validados pelo tempo de execução antes de serem definidos para o dispositivo.<br/> Direct3D 9-Sim<br/> Direct3D 10-Sim<br/>                                                                                                                                                                                                                                                                      |
| <span id="D3DXSHADER_USE_LEGACY_D3DX9_31_DLL"></span><span id="d3dxshader_use_legacy_d3dx9_31_dll"></span><dl> <dt>**D3DXSHADER \_ USAR \_ D3DX9 de/LD herdado de \_ \_ 31 \_ dll**</dt> <dt></dt> </dl>                     | Habilite o uso do compilador HLSL do Direct3D 9 original. OCT2006 \_ d3dx9 \_ 31 \_x86.cab ou OCT2006 \_ d3dx9 \_ 31 \_x64.cab deve ser incluído como parte do Redist de aplicativos. Esse sinalizador é necessário para compilar \_ \_ sombreadores PS 1 x sem usar o sinalizador promocional para o PS \_ 2 \_ 0. Especificar esse sinalizador ao obter uma interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) faz com que as chamadas subsequentes para [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) e [**CompileShader**](id3dxeffectcompiler--compileshader.md) por meio desse objeto usem o compilador herdado.<br/> Direct3D 9-Sim<br/> Direct3D 10-não<br/> |



**Sinalizadores do Assembler**

Os sinalizadores do assembler são usados pelo sistema de efeitos para otimizar o sombreador e o código do assembly de efeito.



| Constante                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DXSHADER_DEBUG"></span><span id="d3dxshader_debug"></span><dl> <dt>**\_Depuração D3DXSHADER**</dt> </dl>                                                          | Insira o nome de arquivo de depuração, números de linha e informações de tipo e símbolo durante a compilação do sombreador.<br/>                                                                                                                                                                                                                   |
| <span id="D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_ps_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ PS \_ software \_ NOOPT**</dt> </dl> | Force o compilador a Compilar no próximo destino de software mais alto disponível para sombreadores de pixel. Esse sinalizador também desativa as otimizações e a depuração.<br/>                                                                                                                                                  |
| <span id="D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT"></span><span id="d3dxshader_force_vs_software_noopt"></span><dl> <dt>**D3DXSHADER \_ Force \_ vs \_ software \_ NOOPT**</dt> </dl> | Force o compilador a Compilar no próximo destino de software mais alto disponível para os sombreadores de vértice. Esse sinalizador também desativa as otimizações e a depuração.<br/>                                                                                                                                                 |
| <span id="D3DXSHADER_SKIPVALIDATION"></span><span id="d3dxshader_skipvalidation"></span><dl> <dt>**D3DXSHADER \_ SKIPVALIDATION**</dt> </dl>                               | Não valide o código gerado em relação a funcionalidades e restrições conhecidas. Essa opção é recomendada somente ao compilar sombreadores que são conhecidos como trabalho (ou seja, sombreadores que foram compilados antes sem essa opção). Os sombreadores sempre são validados pelo tempo de execução antes de serem definidos para o dispositivo.<br/> |



## <a name="remarks"></a>Comentários

O sistema de efeitos usará **sinalizadores do analisador** quando chamado pelas seguintes funções:

-   [**D3DXCompileShader**](d3dxcompileshader.md)
-   [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md)
-   [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md)

O sistema de efeitos usará os **sinalizadores do compilador** quando chamado pelas seguintes funções:

-   [**D3DXCompileShader**](d3dxcompileshader.md) (ou [**D3DXCompileShaderFromFile**](d3dxcompileshaderfromfile.md) ou [**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md))
-   [**CompileEffect**](id3dxeffectcompiler--compileeffect.md) (ou [**CompileShader**](id3dxeffectcompiler--compileshader.md))

Além disso, você pode usar os **sinalizadores do compilador** ao criar um efeito chamando [**D3DXCreateEffect**](d3dxcreateeffect.md) (ou [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) ou [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)).

-   Se você passar um arquivo. FX não compilado, o sistema de efeitos usará o parâmetro de entrada de sinalizador durante a compilação.
-   Se você passar um efeito compilado, o sistema de efeitos ignorará os sinalizadores do compilador, pois eles não são necessários para carregar o efeito.

O sistema de efeitos usará **sinalizadores do assembler** quando chamado pelas seguintes funções:

-   [**D3DXAssembleShader**](d3dxassembleshader.md)
-   [**D3DXAssembleShaderFromFile**](d3dxassembleshaderfromfile.md)
-   [**D3DXAssembleShaderFromResource**](d3dxassembleshaderfromresource.md)

A aplicação de sinalizadores do **compilador** ou **sinalizadores do ASSEMBLEr** à API incorreta falhará na validação do sombreador. Verifique o valor de retorno do código de erro do Direct3D da função com a ferramenta de pesquisa de erros do DirectX (DXErr.exe) para ajudar a rastrear esse erro. Você pode obter DXErr.exe e aprender sobre ele no SDK do DirectX. Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 
