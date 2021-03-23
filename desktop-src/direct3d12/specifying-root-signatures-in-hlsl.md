---
title: Especificando assinaturas raiz em HLSL
description: A especificação de assinaturas raiz no modelo do sombreador HLSL 5,1 é uma alternativa para especificá-los no código C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236876e22c3e1e0bb849ec1e1bc7d45692c900d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548209"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Especificando assinaturas raiz em HLSL

A especificação de assinaturas raiz no modelo do sombreador HLSL 5,1 é uma alternativa para especificá-los no código C++.

-   [Um exemplo de assinatura raiz HLSL](#an-example-hlsl-root-signature)
    -   [Assinatura de raiz versão 1,0](#root-signature-version-10)
    -   [Assinatura de raiz versão 1,1](#root-signature-version-11)
-   [RootFlags](#rootflags)
-   [Constantes raiz](#root-constants)
-   [Visibilidade](#visibility)
-   [CBV no nível raiz](#root-level-cbv)
-   [SRV de nível raiz](#root-level-srv)
-   [UAV no nível raiz](#root-level-uav)
-   [Tabela de descritores](#descriptor-table)
-   [Amostra estática](#static-sampler)
-   [Compilando uma assinatura raiz do HLSL](#compiling-an-hlsl-root-signature)
-   [Manipulando assinaturas raiz com o compilador FXC](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Observações](#notes)
-   [Tópicos relacionados](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Um exemplo de assinatura raiz HLSL

Uma assinatura raiz pode ser especificada em HLSL como uma cadeia de caracteres. A cadeia de caracteres contém uma coleção de cláusulas separadas por vírgulas que descrevem os componentes constituintes da assinatura raiz. A assinatura raiz deve ser idêntica em sombreadores para qualquer um dos objetos de estado de pipeline (PSO). Veja um exemplo:

### <a name="root-signature-version-10"></a>Assinatura de raiz versão 1,0

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

### <a name="root-signature-version-11"></a>Assinatura de raiz versão 1,1

A [assinatura de raiz versão 1,1](root-signature-version-1-1.md) permite otimizações de driver em dados e descritores de assinatura raiz.

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Essa definição daria a seguinte assinatura de raiz, observando:

-   O uso de parâmetros padrão.
-   B0 e (B0, espaço = 1) não entram em conflito
-   U0 só é visível para o sombreador Geometry
-   U4 e U5 são alias para o mesmo descritor em um heap

![uma assinatura raiz especificada usando o idioma do sombreador de alto nível](images/hlsl-root-signature.png)

A linguagem de assinatura raiz HLSL corresponde de forma mais próxima às APIs de assinatura raiz do C++ e tem uma potência expressiva equivalente. A assinatura raiz é especificada como uma sequência de cláusulas, separadas por vírgula. A ordem das cláusulas é importante, pois a ordem de análise determina a posição do slot na assinatura raiz. Cada cláusula usa um ou mais parâmetros nomeados. No entanto, a ordem dos parâmetros não é importante.

## <a name="rootflags"></a>RootFlags

A cláusula opcional *RootFlags* usa 0 (o valor padrão para indicar nenhum sinalizador) ou um ou vários valores de sinalizadores de raiz predefinidos, conectados por meio do \| operador ou ' '. Os valores de sinalizador raiz permitidos são definidos [**por \_ \_ \_ sinalizadores de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

Por exemplo:

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Constantes raiz

A cláusula *RootConstants* Especifica constantes raiz na assinatura raiz. Dois parâmetros obrigatórios são: *num32BitConstants* e *bReg* (o registro correspondente ao *BaseShaderRegister* em APIs do C++) do *CBuffer*. Os parâmetros Space (*RegisterSpace* em c++ APIs) e Visibility (*ShaderVisibility* em c++) são opcionais e os valores padrão são:

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Por exemplo:

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Visibilidade

Visibility é um parâmetro opcional que pode ter um dos valores da [**\_ \_ visibilidade do sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

\_A visibilidade \_ do sombreador todos transmite os argumentos raiz para todos os sombreadores. Em algum hardware, isso não tem nenhum custo, mas em outro hardware há um custo para bifurcar os dados para todos os estágios do sombreador. Definir uma das opções, como \_ vértice de visibilidade do sombreador \_ , limita o argumento raiz a um único estágio de sombreador.

A configuração de argumentos raiz para estágios de sombreador único permite que o mesmo nome de associação seja usado em diferentes estágios. Por exemplo, uma associação SRV de `t0,SHADER_VISIBILITY_VERTEX` e a associação SRV de `t0,SHADER_VISIBILITY_PIXEL` seriam válidas. Mas se a configuração de visibilidade era `t0,SHADER_VISIBILITY_ALL` para uma das associações, a assinatura raiz seria inválida.

## <a name="root-level-cbv"></a>CBV no nível raiz

A `CBV` cláusula (exibição de buffer de constante) especifica uma entrada reg de buffer constante de nível de raiz b. Observe que esta é uma entrada escalar; Não é possível especificar um intervalo para o nível raiz.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV de nível raiz

A `SRV` cláusula (exibição de recurso do sombreador) especifica uma entrada reg t-Register do registro no nível raiz. Observe que esta é uma entrada escalar; Não é possível especificar um intervalo para o nível raiz.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV no nível raiz

A `UAV` cláusula (exibição de acesso não ordenado) especifica uma entrada reg do UAV no nível da raiz. Observe que esta é uma entrada escalar; Não é possível especificar um intervalo para o nível raiz.

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Por exemplo:

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>Tabela de descritores

A `DescriptorTable` cláusula é, em si, uma lista de cláusulas de tabela de descritores separados por vírgulas, bem como um parâmetro de visibilidade opcional. As cláusulas de *descriptortable* incluem cbv, SRV, UAV e amostra. Observe que seus parâmetros diferem das cláusulas de nível raiz.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

A tabela de descritores `CBV` tem a seguinte sintaxe:

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Por exemplo:

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

O parâmetro obrigatório *bReg* especifica o Reg de início do intervalo de CBuffer. O parâmetro *numDescriptors* especifica o número de descritores no intervalo CBuffer contíguo; o valor padrão é 1. A entrada declara um intervalo de CBuffer ` [Reg, Reg + numDescriptors - 1]` quando *numDescriptors* é um número. Se *numDescriptors* for igual a "unbounded", o intervalo será `[Reg, UINT_MAX]` , o que significa que o aplicativo deve garantir que ele não faz referência a uma área fora de limites. O campo de *deslocamento* representa o parâmetro *OffsetInDescriptorsFromTableStart* nas APIs do C++, ou seja, o deslocamento (em descritores) do início da tabela. Se o deslocamento for definido como DESCRITOr de deslocamento de intervalo de descrição \_ \_ \_ (o padrão), significa que o intervalo é diretamente após o intervalo anterior. No entanto, a inserção de deslocamentos específicos permite que os intervalos se sobreponham, permitindo o registro de alias.

A tabela de descritores `SRV` tem a seguinte sintaxe:

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Isso é semelhante à entrada da tabela de descritores `CBV` , exceto pelo intervalo especificado para exibições de recursos do sombreador.

A tabela de descritores `UAV` tem a seguinte sintaxe:

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Isso é semelhante à entrada da tabela de descritores `CBV` , exceto pelo intervalo especificado para exibições de acesso não ordenado.

A tabela de descritores `Sampler` tem a seguinte sintaxe:

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

Isso é semelhante à entrada da tabela de descritores `CBV` , exceto pelo intervalo especificado para os exemplos de sombreador. Observe que os exemplos não podem ser misturados com outros tipos de descritores na mesma tabela de descrição (já que estão em um heap de descritor separado).

## <a name="static-sampler"></a>Amostra estática

A amostra estática representa a [**estrutura \_ \_ \_ desc de amostra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) . O parâmetro obrigatório para *StaticSampler* é um Reg de amostras de s-Register. Outros parâmetros são opcionais com valores padrão mostrados abaixo. A maioria dos campos aceita um conjunto de enums predefinidos.

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

Por exemplo:

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

As opções de parâmetro são muito semelhantes às chamadas da API do C++, exceto a *BorderColor*, que é restrita a uma enumeração em HLSL.

O campo de filtro pode ser um [**dos \_ filtros D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).

Os campos de endereço podem ser um dos [**\_ modos de \_ endereço \_ de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).

A função de comparação pode ser uma das [**D3D12 de \_ comparação \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).

O campo de cor da borda pode ser uma das [**\_ \_ \_ cores de borda estática D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).

A visibilidade pode ser uma das [**D3D12 do \_ sombreador \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

## <a name="compiling-an-hlsl-root-signature"></a>Compilando uma assinatura raiz do HLSL

Há dois mecanismos para compilar uma assinatura raiz HLSL. Primeiro, é possível anexar uma cadeia de caracteres de assinatura raiz a um sombreador específico por meio do atributo *RootSignature* (no exemplo a seguir, usando o ponto de entrada **MyRS1** ):

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

O compilador criará e verificará o blob de assinatura raiz para o sombreador e o inserirá junto com o código de byte do sombreador no blob do sombreador. O compilador dá suporte à sintaxe de assinatura raiz para o modelo de sombreador 5,0 e superior. Se uma assinatura raiz for inserida em um sombreador do modelo do sombreador 5,0 e esse sombreador for enviado para o tempo de execução D3D11, em oposição ao D3D12, a parte da assinatura raiz será silenciosamente ignorada pelo D3D11.

O outro mecanismo é criar um blob de assinatura de raiz autônoma, talvez reutilizá-lo com um grande conjunto de sombreadores, economizando espaço. A [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc) (FXC) dá suporte aos modelos de sombreador **rootsig \_ 1 \_ 0** e **rootsig \_ 1 \_ 1** . O nome da cadeia de caracteres de definição é especificado por meio do argumento/E usual. Por exemplo:

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Observe que a cadeia de caracteres de assinatura de raiz também pode ser passada na linha de comando, por exemplo,/D MyRS1 = "...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Manipulando assinaturas raiz com o compilador FXC

O compilador FXC cria o código de byte de sombreador de arquivos de origem HLSL. Há muitos parâmetros opcionais para esse compilador, consulte a [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc).

Para gerenciar assinaturas raiz criadas pelo HLSL, a tabela a seguir fornece alguns exemplos de como usar o FXC.



| Linha | Linha de comando                                                                 | Descrição                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Compila um sombreador para o destino do pixel shader 5,1, a origem do sombreador está no arquivo shaderWithRootSig. HLSL, que inclui uma assinatura raiz. O sombreador e a assinatura raiz são compilados como BLOBs separados no arquivo binário RS1. FXO.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Extrai a assinatura raiz do arquivo criado pela linha 1, portanto, o arquivo RS1. RS. FXO contém apenas uma assinatura raiz.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Remove a assinatura raiz do arquivo criado pela linha 1, de modo que o arquivo RS1.. FXO contém um sombreador sem assinatura raiz.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Combina um sombreador e uma assinatura raiz que estão em arquivos separados em um arquivo binário que contém os dois BLOBs. Neste exemplo, RS1. New. fx0 seria idêntico a RS1. fx0 na linha 1.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Cria um arquivo binário de assinatura de raiz autônoma de uma fonte que pode conter mais do que apenas uma assinatura raiz. Observe o \_ destino rootsig 1 \_ 0 e que RS1 é o nome da cadeia de caracteres de macro da assinatura raiz ( \# definir) no arquivo HLSL. |



 

A funcionalidade disponível por meio do FXC também está disponível programaticamente usando a função [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) . Essa chamada compila um sombreador com uma assinatura raiz ou uma assinatura raiz autônoma (definindo o \_ destino rootsig 1 \_ 0). [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) e [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) podem extrair e anexar assinaturas raiz a um blob existente.\_ \_ A assinatura raiz do blob do D3D \_ é usada para especificar o tipo de parte do blob de assinatura raiz. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) remove a assinatura raiz (usando o \_ sinalizador de \_ assinatura raiz da faixa D3DCOMPILER \_ ) do blob.

## <a name="notes"></a>Observações

> [!Note]  
> Enquanto a compilação offline de sombreadores é altamente recomendável, se os sombreadores precisarem ser compilados em tempo de execução, consulte os comentários para [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).

 

> [!Note]  
> Os ativos HLSL existentes não precisam ser alterados para lidar com as assinaturas raiz a serem usadas com eles.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Indexação dinâmica usando HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Recursos do HLSL Shader Model 5,1 para Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Associação de recursos](resource-binding.md)
</dt> <dt>

[Associação de recursos em HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> <dt>

[Modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Valor de referência de estêncil especificado do sombreador](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Cargas de exibição de acesso não ordenado digitado](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 