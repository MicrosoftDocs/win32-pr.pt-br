---
description: Os aplicativos usam os métodos da interface ID3DX10Mesh para manipular objetos de malha.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: Interface ID3DX10Mesh (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddf0876928f85debded1645b9a22de790917017
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105770644"
---
# <a name="id3dx10mesh-interface"></a>Interface ID3DX10Mesh

Os aplicativos usam os métodos da interface ID3DX10Mesh para manipular objetos de malha.

## <a name="members"></a>Membros

A interface **ID3DX10Mesh** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Mesh** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10Mesh** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | Cria uma nova malha e a preenche com os dados de uma malha carregada anteriormente.<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | Confirme as alterações feitas em uma malha para o dispositivo para que as alterações possam ser processadas. Isso deve ser chamado depois que os dados de uma malha são alterados e antes de serem renderizados. Uma malha não pode ser renderizada a menos que seja confirmada no dispositivo. Consulte Observações.<br/>                                                                         |
| [**Descartar**](id3dx10mesh-discard.md)                                                   | Remove os dados de malha do dispositivo que foi confirmado no dispositivo (com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Desenha um subconjunto de uma malha.<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | Desenhe várias instâncias do mesmo subconjunto de uma malha.<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | Gere um buffer de atributo dos dados na tabela de atributos da malha. Um buffer de atributo é outro formato para armazenar os dados na tabela de atributos. O buffer de atributo e a tabela de atributos são estruturas de dados internas na malha.<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | Adiciona dados de adjacência ao buffer de índice da malha. Quando a malha é enviada para um sombreador de geometria que usa dados de adjacência, é necessário que o buffer de índice da malha contenha dados de adjacência.<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Acesse o buffer de adjacência da malha.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | Acesse o buffer de atributo da malha.<br/>                                                                                                                                                                                                                                                                                       |
| [**Getattributetable**](id3dx10mesh-getattributetable.md)                               | Recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Acesse o buffer de índice da malha depois que ele tiver sido confirmado no dispositivo com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Isso é diferente de [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), que retorna o buffer de índice antes de ser confirmado no dispositivo.<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Acesse o buffer de vértice da malha depois que ele tiver sido confirmado no dispositivo com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Isso é diferente de [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que retorna o buffer de vértice antes de ser confirmado no dispositivo.<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | Recupera o número de faces na malha.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Acesse os sinalizadores de criação da malha.<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | Recupera os dados em um buffer de índice.<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Obtenha o buffer do representante do ponto da malha.<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Recupera o buffer de vértice associado à malha.<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | Obtenha o número de buffers de vértice na malha.<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | Obtenha o número de vértices na malha. Uma malha pode conter vários buffers de vértice (ou seja, um buffer de vértice pode conter todos os dados de posição, outro pode incluir todos os dados de coordenadas de textura, etc.), no entanto, cada buffer de vértice conterá o mesmo número de elementos.<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | Acesse a descrição do vértice passada para [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). A descrição do vértice descreve o layout dos buffers de vértice da malha.<br/>                                                                                                                                                   |
| [**Formam**](id3dx10mesh-intersect.md)                                               | Determina se um raio intersecciona com essa malha.<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | Determina se um raio intersecciona com um subconjunto dessa malha.<br/>                                                                                                                                                                                                                                                                |
| [**Otimizar**](id3dx10mesh-optimize.md)                                                 | Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | Defina os dados de adjacência da malha.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | Defina os dados de atributo da malha.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | Define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | Defina os dados de índice da malha.<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | Defina os dados do representante do ponto para a malha.<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | Defina dados de vértice em um dos buffers de vértice da malha.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

Para obter a interface ID3DX10Mesh, chame [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
