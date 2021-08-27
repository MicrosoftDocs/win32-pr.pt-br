---
description: Os aplicativos usam os métodos da interface ID3DX10Mesh para manipular objetos de malha.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: Interface ID3DX10Mesh (D3DX10.h)
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
ms.openlocfilehash: 2506191db941eee0a046d52f64aaeeb0f642f11dd35e42d6b49c4b5f5f457d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096646"
---
# <a name="id3dx10mesh-interface"></a>Interface ID3DX10Mesh

Os aplicativos usam os métodos da interface ID3DX10Mesh para manipular objetos de malha.

## <a name="members"></a>Membros

A interface **ID3DX10Mesh** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Mesh** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10Mesh** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | Cria uma nova malha e a preenche com os dados de uma malha carregada anteriormente.<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | Fazer commit das alterações feitas em uma malha no dispositivo para que as alterações possam ser renderizadas. Isso deve ser chamado depois que os dados de uma malha são alterados e antes de serem renderizados. Uma malha não pode ser renderizada, a menos que esteja comprometida com o dispositivo. Consulte Observações.<br/>                                                                         |
| [**Descartar**](id3dx10mesh-discard.md)                                                   | Remove os dados de malha do dispositivo que foi confirmado para o dispositivo (com [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Desenha um subconjunto de uma malha.<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | Desenhar várias instâncias do mesmo subconjunto de uma malha.<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Gere uma lista de bordas de malha, bem como uma lista de rostos que compartilham cada borda.<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | Gere um buffer de atributo dos dados na tabela de atributos da malha. Um buffer de atributo é outro formato para armazenar os dados na tabela de atributos. O buffer de atributo e a tabela de atributos são estruturas de dados internas na malha.<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | Adiciona dados de adjacency ao buffer de índice da malha. Quando a malha deve ser enviada para um sombreador de geometria que recebe dados de adjacency, é necessário que o buffer de índice da malha contenha dados de adjacency.<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Acesse o buffer de adjacency da malha.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | Acesse o buffer de atributo da malha.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | Recupera uma tabela de atributo para uma malha ou o número de entradas armazenadas em uma tabela de atributo para uma malha.<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Acesse o buffer de índice da malha depois que ele tiver sido confirmado no dispositivo com [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Isso é diferente de [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), que retorna o buffer de índice antes de ser comprometido com o dispositivo.<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Acesse o buffer de vértice da malha depois que ele tiver sido confirmado no dispositivo com [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Isso é diferente de [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que retorna o buffer de vértice antes de ser confirmado no dispositivo.<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | Recupera o número de rostos na malha.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Acesse os sinalizadores de criação da malha.<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | Recupera os dados em um buffer de índice.<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Obter o buffer de representante de ponto da malha.<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Recupera o buffer de vértice associado à malha.<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | Obter o número de buffers de vértice na malha.<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | Obter o número de vértices na malha. Uma malha pode conter vários buffers de vértice (ou seja, um buffer de vértice pode conter todos os dados de posição, outro pode conter todos os dados de coordenadas de textura etc.), no entanto, cada buffer de vértice conterá o mesmo número de elementos.<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | Acesse a descrição do vértice passada [**para D3DX10CreateMesh.**](d3d10-d3dx10createmesh.md) A descrição do vértice descreve o layout dos buffers de vértice da malha.<br/>                                                                                                                                                   |
| [**Intersect**](id3dx10mesh-intersect.md)                                               | Determina se um raio intersecção com essa malha.<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | Determina se um raio intersecção com um subconjunto dessa malha.<br/>                                                                                                                                                                                                                                                                |
| [**Otimizar**](id3dx10mesh-optimize.md)                                                 | Gera uma nova malha com rostos e vértices reordenados para otimizar o desempenho do desenho.<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | Definir os dados de adjacency da malha.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | Definir os dados de atributo da malha.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | Define a tabela de atributo para uma malha e o número de entradas armazenadas na tabela.<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | Definir os dados de índice da malha.<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | Definir os dados de representante de ponto para a malha.<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | Definir dados de vértice em um dos buffers de vértice da malha.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

Para obter a interface ID3DX10Mesh, chame [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
