---
title: Criando uma assinatura raiz
description: As assinaturas raiz são uma estrutura de dados complexa que contém estruturas aninhadas.
ms.assetid: 565B28C1-DBD1-42B6-87F9-70743E4A2E4A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9660f35c349342d147a61a6b4ce9c02a4a1abab
ms.sourcegitcommit: 65af948af39d1a31885a1b688f5dbfe955d7eba1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/18/2020
ms.locfileid: "104548226"
---
# <a name="creating-a-root-signature"></a>Criando uma assinatura raiz

As assinaturas raiz são uma estrutura de dados complexa que contém estruturas aninhadas. Eles podem ser definidos programaticamente usando a definição de estrutura de dados abaixo (que inclui métodos para ajudar a inicializar Membros). Como alternativa, eles podem ser criados na HLSL (linguagem de sombreamento de alto nível), dando a vantagem de que o compilador será validado antes que o layout seja compatível com o sombreador.

A API para criar uma assinatura raiz usa uma versão serializada (autocontida, ponteiro livre) da descrição do layout descrita abaixo. Um método é fornecido para gerar essa versão serializada da estrutura de dados do C++, mas outra maneira de obter uma definição de assinatura raiz serializada é recuperá-la de um sombreador que foi compilado com uma assinatura raiz.

Se você quiser tirar proveito das otimizações de driver para os dados e descritores de assinatura raiz, consulte a [assinatura raiz versão 1,1](root-signature-version-1-1.md)

-   [Tipos de associação de tabela de descritores](#descriptor-table-bind-types)
-   [Intervalo de descritores](#descriptor-range)
-   [Layout da tabela de descritores](#descriptor-table-layout)
-   [Constantes raiz](#root-constants)
-   [Descritor raiz](#root-descriptor)
-   [Visibilidade do sombreador](#shader-visibility)
-   [Definição de assinatura raiz](#root-signature-definition)
-   [Serialização/desserialização da estrutura de dados da assinatura raiz](/windows)
-   [API de criação de assinatura raiz](#root-signature-creation-api)
-   [Assinatura de raiz em objetos de estado do pipeline](#root-signature-in-pipeline-state-objects)
-   [Código para definir uma assinatura raiz da versão 1,1](#code-for-defining-a-version-11-root-signature)
-   [Tópicos relacionados](#related-topics)

## <a name="descriptor-table-bind-types"></a>Tipos de associação de tabela de descritores

O [**tipo de \_ \_ intervalo do \_ descritor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) de enumeração D3D12 define os tipos de descritores que podem ser referenciados como parte de uma definição de layout de tabela de descritor.

É um intervalo para que, por exemplo, se parte de uma tabela de descritor tenha 100 SRVs, esse intervalo possa ser declarado em uma entrada em vez de 100. Portanto, uma definição de tabela de descritor é uma coleção de intervalos.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_TYPE
{
  D3D12_DESCRIPTOR_RANGE_TYPE_SRV,
  D3D12_DESCRIPTOR_RANGE_TYPE_UAV,
  D3D12_DESCRIPTOR_RANGE_TYPE_CBV,
  D3D12_DESCRIPTOR_RANGE_TYPE_SAMPLER
} D3D12_DESCRIPTOR_RANGE_TYPE;
```

## <a name="descriptor-range"></a>Intervalo de descritores

A estrutura do [**\_ \_ intervalo do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) define um intervalo de descripdores de um determinado tipo (como SRVs) em uma tabela de descritores.

A `D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND` macro normalmente pode ser usada para o `OffsetInDescriptorsFromTableStart` parâmetro do [**\_ \_ intervalo do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Isso significa acrescentar o intervalo do descritor que está sendo definido após o anterior na tabela de descritores. Se o aplicativo quiser descritores de alias ou por algum motivo desejar ignorar os slots, ele poderá ser definido `OffsetInDescriptorsFromTableStart` para qualquer deslocamento desejado. A definição de intervalos sobrepostos de tipos diferentes é inválida.

O conjunto de registros de sombreador especificado pela combinação de `RangeType` , `NumDescriptors` , `BaseShaderRegister` e `RegisterSpace` não pode entrar em conflito ou se sobrepor em quaisquer declarações em uma assinatura raiz que tenha [**\_ \_ visibilidade de sombreador D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) comum (consulte a seção de visibilidade do sombreador abaixo).

## <a name="descriptor-table-layout"></a>Layout da tabela de descritores

A estrutura da [**\_ \_ \_ tabela do descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) declara o layout de uma tabela de descritores como uma coleção de intervalos de descritores que aparecem um após o outro em um heap de descritor. Os exemplos não são permitidos na mesma tabela de descritores que CBV/UAV/SRVs.

Essa estrutura é usada quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_DESCRIPTOR_TABLE` .

Para definir uma tabela de descritor de gráficos (CBV, SRV, UAV, Sample), use [**ID3D12GraphicsCommandList:: SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable).

Para definir uma tabela de descritor de computação, use [**ID3D12GraphicsCommandList:: SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable).

## <a name="root-constants"></a>Constantes raiz

A estrutura de [**\_ \_ constantes raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) declara constantes embutidas na assinatura raiz que aparecem em sombreadores como um buffer constante.

Essa estrutura é usada quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_32BIT_CONSTANTS` .

## <a name="root-descriptor"></a>Descritor raiz

A estrutura do [**\_ \_ descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) declara os descritores (que aparecem em sombreadores) embutidos na assinatura raiz.

Essa estrutura é usada quando o tipo de slot de assinatura raiz é definido como `D3D12_ROOT_PARAMETER_TYPE_CBV` , `D3D12_ROOT_PARAMETER_TYPE_SRV` ou `D3D12_ROOT_PARAMETER_TYPE_UAV` .

## <a name="shader-visibility"></a>Visibilidade do sombreador

O membro de [**D3D12 \_ de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) definido no parâmetro de visibilidade do sombreador do [**\_ \_ parâmetro raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) determina quais sombreadores veem o conteúdo de um determinado slot de assinatura raiz. A computação sempre usa \_ tudo (já que há apenas um estágio ativo). Os gráficos podem escolher, mas se usar \_ todos, todos os estágios do sombreador verão o que estiver associado ao slot de assinatura raiz.

Um uso da visibilidade do sombreador é ajudar com os sombreadores que são criados esperando associações diferentes por estágio do sombreador usando um namespace sobreposto. Por exemplo, um sombreador de vértice pode declarar:

 

Texture2D foo: Register (T0); "

 

e o sombreador de pixel também pode declarar:

 

Barra de Texture2D: registro (T0);

Se o aplicativo fizer uma associação de assinatura raiz para a visibilidade T0 \_ , ambos os sombreadores verão a mesma textura. Se o sombreador definir realmente deseja que cada sombreador Veja texturas diferentes, ele poderá definir 2 slots de assinatura raiz com \_ vértice de visibilidade e \_ pixel. Não importa qual a visibilidade está em um slot de assinatura raiz, ela sempre tem o mesmo custo (custo somente dependendo do tipo de Slottype) em relação a um tamanho de assinatura de raiz máximo fixo.

Em hardware D3D11 de baixo nível, \_ a visibilidade do sombreador também é levada em conta usada ao validar os tamanhos das tabelas de descritores em um layout raiz, já que alguns hardwares D3D11 podem dar suporte apenas a uma quantidade máxima de associações por etapa. Essas restrições só são impostas durante a execução em hardware de camada baixa e não limitam um hardware mais moderno.

Se uma assinatura de raiz tiver várias tabelas de descritores definidas que se sobrepõem em namespace (o registro de associações para o sombreador) e qualquer uma delas especificar \_ tudo para visibilidade, o layout será inválido (a criação falhará).

## <a name="root-signature-definition"></a>Definição de assinatura raiz

A [**estrutura \_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) pode conter tabelas de descritores e constantes embutidas, cada tipo de slot definido pela estrutura de [**\_ \_ parâmetro raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) e o tipo de [**\_ parâmetro de raiz \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_parameter_type)de enumeração.

Para iniciar um slot de assinatura raiz, consulte os **métodos \* \* \* SetComputeRoot** e **SetGraphicsRoot \* \* \*** de [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

Os exemplos estáticos são descritos na assinatura raiz usando a estrutura de [**\_ \_ amostra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

Um número de sinalizadores limita o acesso de determinados sombreadores à assinatura raiz, consulte [**\_ \_ \_ sinalizadores de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

## <a name="root-signature-data-structure-serialization--deserialization"></a>Serialização/desserialização da estrutura de dados da assinatura raiz

Os métodos descritos nesta seção são exportados por D3D12Core.dll e fornecem métodos para serialização e desserialização de uma estrutura de dados de assinatura raiz.

O formulário serializado é o que é passado para a API ao criar uma assinatura raiz. Se um sombreador tiver sido criado com uma assinatura de raiz nele (quando esse recurso for adicionado), o sombreador compilado conterá uma assinatura de raiz serializada já.

Se um aplicativo gerar um procedimento de uma estrutura de dados [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) , ele deverá tornar o formulário serializado usando [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature). A saída de que pode ser passada em [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature).

Se um aplicativo já tiver uma assinatura raiz serializada ou tiver um sombreador compilado que contenha uma assinatura raiz e desejar descobrir programaticamente a definição de layout (conhecida como "reflexão"), [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) poderá ser chamado. Isso gera uma interface [**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) , que contém um método para retornar a estrutura de dados [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) desserializada. A interface possui o tempo de vida da estrutura de dados desserializada.

## <a name="root-signature-creation-api"></a>API de criação de assinatura raiz

A API [**ID3D12Device:: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) usa uma versão serializada de uma assinatura raiz.

## <a name="root-signature-in-pipeline-state-objects"></a>Assinatura de raiz em objetos de estado do pipeline

Os métodos para criar o estado do pipeline ([**ID3D12Device:: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device:: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ) usam uma interface opcional [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) como um parâmetro de entrada (armazenado em uma estrutura [**desc de estado de \_ pipeline de elementos gráficos \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ). Isso substituirá qualquer assinatura raiz que já esteja nos sombreadores.

Se uma assinatura de raiz for passada em um dos métodos de criação de estado de pipeline, essa assinatura raiz será validada em relação a todos os sombreadores no PSO para compatibilidade e dada ao driver a ser usado com todos os sombreadores. Se qualquer um dos sombreadores tiver uma assinatura de raiz diferente, ele será substituído pela assinatura raiz passada na API. Se uma assinatura raiz não for passada, todos os sombreadores passados deverão ter uma assinatura raiz e deverão corresponder – isso será fornecido ao driver. A definição de um PSO em uma lista de comandos ou pacote não altera a assinatura raiz. Isso é realizado pelos métodos [**SetGraphicsRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature) e [**SetComputeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature). No momento em que o empate (Graphics)/dispatch (computação) é invocado, o aplicativo deve garantir que o PSO atual corresponda à assinatura raiz atual; caso contrário, o comportamento será indefinido.

## <a name="code-for-defining-a-version-11-root-signature"></a>Código para definir uma assinatura raiz da versão 1,1

O exemplo a seguir mostra como criar uma assinatura de raiz com o seguinte formato:



|                        |                                                |                                              |
|------------------------|------------------------------------------------|----------------------------------------------|
| **RootParameterIndex** | **Contents**                                   |                                              |
| \[0\]                  | Constantes raiz: {B2}                         | (1 CBV)                                      |
| \[1\]                  | Tabela de descritores: {T2-T7, U0-U3}             | (6 SRVs + 4 UAVs)                            |
| \[2\]                  | CBV raiz: {B0}                               | (1 CBV, dados estáticos)                         |
| \[3\]                  | Tabela de descritores: {S0-S1}                    | (2 amostras)                                 |
| \[4\]                  | Tabela de descritores: {T8}           | (não limitado \# de SRVs, descritores voláteis) |
| \[5\]                  | Tabela de descritores: {(T0, space1) – não associado} | (não limitado \# de SRVs, descritores voláteis) |
| \[6\]                  | Tabela de descritores: {B1}                       | (1 CBV, dados estáticos)                         |



 

Se a maioria das partes da assinatura raiz for usada na maior parte do tempo, pode ser melhor ter que mudar a assinatura raiz com muita frequência. Os aplicativos devem classificar as entradas na assinatura raiz da alteração mais frequente para o mínimo. Quando um aplicativo altera as associações para qualquer parte da assinatura raiz, o driver pode ter que fazer uma cópia de algum ou de todo o estado de assinatura raiz, o que pode se tornar um custo não trivial quando multiplicado por muitas alterações de estado.

Além disso, a assinatura raiz definirá uma amostra estática que faz a filtragem de textura anisotropic no sombreador de registro S3.

Depois que essa assinatura raiz é associada, as tabelas de descritores, CBV e constantes raiz podem ser atribuídas ao \[ espaço de parâmetro 0.. 6 \] . por exemplo, as tabelas de descritores (intervalos em um heap de descritor) podem ser associadas a cada um dos parâmetros de raiz \[ 1 \] e \[ 3.. 6 \] .

``` syntax
CD3DX12_DESCRIPTOR_RANGE1 DescRange[6];

DescRange[0].Init(D3D12_DESCRIPTOR_RANGE_SRV,6,2); // t2-t7
DescRange[1].Init(D3D12_DESCRIPTOR_RANGE_UAV,4,0); // u0-u3
DescRange[2].Init(D3D12_DESCRIPTOR_RANGE_SAMPLER,2,0); // s0-s1
DescRange[3].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,8, 0,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); // t8-unbounded
DescRange[4].Init(D3D12_DESCRIPTOR_RANGE_SRV,-1,0,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE); 
                                                            // (t0,space1)-unbounded
DescRange[5].Init(D3D12_DESCRIPTOR_RANGE_CBV,1,1,
                  D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC); // b1

CD3DX12_ROOT_PARAMETER1 RP[7];

RP[0].InitAsConstants(3,2); // 3 constants at b2
RP[1].InitAsDescriptorTable(2,&DescRange[0]); // 2 ranges t2-t7 and u0-u3
RP[2].InitAsConstantBufferView(0, 0, 
                               D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC); // b0
RP[3].InitAsDescriptorTable(1,&DescRange[2]); // s0-s1
RP[4].InitAsDescriptorTable(1,&DescRange[3]); // t8-unbounded
RP[5].InitAsDescriptorTable(1,&DescRange[4]); // (t0,space1)-unbounded
RP[6].InitAsDescriptorTable(1,&DescRange[5]); // b1

CD3DX12_STATIC_SAMPLER StaticSamplers[1];
StaticSamplers[0].Init(3, D3D12_FILTER_ANISOTROPIC); // s3
CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC RootSig(7,RP,1,StaticSamplers);
ID3DBlob* pSerializedRootSig;
CheckHR(D3D12SerializeVersionedRootSignature(&RootSig,pSerializedRootSig)); 

ID3D12RootSignature* pRootSignature;
hr = CheckHR(pDevice->CreateRootSignature(
    pSerializedRootSig->GetBufferPointer(),pSerializedRootSig->GetBufferSize(),
    __uuidof(ID3D12RootSignature),
    &pRootSignature));
```

O código a seguir ilustra como a assinatura raiz acima pode ser usada em uma lista de comandos gráficos.

``` syntax
InitializeMyDescriptorHeapContentsAheadOfTime(); // for simplicity of the 
                                                 // example
CreatePipelineStatesAhreadOfTime(pRootSignature); // The root signature is passed into 
                                     // shader / pipeline state creation
...

ID3D12DescriptorHeap* pHeaps[2] = {pCommonHeap, pSamplerHeap};
pGraphicsCommandList->SetDescriptorHeaps(pHeaps,2);
pGraphicsCommandList->SetGraphicsRootSignature(pRootSignature);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        6,heapOffsetForMoreData,DescRange[5].NumDescriptors);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(5,heapOffsetForMisc,5000); 
pGraphicsCommandList->SetGraphicsRootDescriptorTable(4,heapOffsetForTerrain,20000);
pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                        3,heapOffsetForSamplers,DescRange[2].NumDescriptors);
pGraphicsCommandList->SetComputeRootConstantBufferView(2,pDynamicCBHeap,&CBVDesc);

MY_PER_DRAW_STUFF stuff;
InitMyPerDrawStuff(&stuff);
pGraphicsCommandList->SetSetGraphicsRoot32BitConstants(
                        0,&stuff,0,RTSlot[0].Constants.Num32BitValues);

SetMyRTVAndOtherMiscBindings();

for(UINT i = 0; i < numObjects; i++)
{
    pGraphicsCommandList->SetPipelineState(PSO[i]);
    pGraphicsCommandList->SetGraphicsRootDescriptorTable(
                    1,heapOffsetForFooAndBar[i],DescRange[1].NumDescriptors);
    pGraphicsCommandList->SetGraphicsRoot32BitConstant(0,&i,1,drawIDOffset);
    SetMyIndexBuffers(i);
    pGraphicsCommandList->DrawIndexedInstanced(...);
}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> <dt>

[Especificando assinaturas raiz em HLSL](specifying-root-signatures-in-hlsl.md)
</dt> <dt>

[Usando uma assinatura de raiz](using-a-root-signature.md)
</dt> </dl>

 

 
