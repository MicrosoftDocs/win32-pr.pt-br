---
description: Esta seção contém informações de referência para as interfaces de modelo de objeto de componente (COM) fornecidas pela biblioteca do utilitário D3DX. As interfaces a seguir são usadas com a biblioteca do utilitário D3DX.
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: Interfaces D3DX (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e0fc152468efec4e33fd6a3ab467d211cfbef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752415"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a>Interfaces D3DX (gráficos do Direct3D 10)

Esta seção contém informações de referência para as interfaces de modelo de objeto de componente (COM) fornecidas pela biblioteca do utilitário D3DX. As interfaces a seguir são usadas com a biblioteca do utilitário D3DX.



| Interfaces                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface ID3DX10DataLoader**](id3dx10dataloader.md)       | Objeto de carregamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para carregar dados de forma assíncrona.<br/>                                                                                                                                                                                                                                                                                                   |
| [**Interface ID3DX10DataProcessor**](id3dx10dataprocessor.md) | Objeto de processamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para processar dados carregados de forma assíncrona.<br/>                                                                                                                                                                                                                                                                                      |
| [**Interface ID3DX10Font**](id3dx10font.md)                   | A interface ID3DX10Font encapsula as texturas e os recursos necessários para processar uma fonte específica em um dispositivo específico.<br/>                                                                                                                                                                                                                                                                                                |
| [**Interface ID3DX10Mesh**](id3dx10mesh.md)                   | Os aplicativos usam os métodos da interface ID3DX10Mesh para manipular objetos de malha.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**Interface ID3DX10MeshBuffer**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Interface ID3DX10SkinInfo**](id3dx10skininfo.md)           | O ID3DX10SkinInfo permite otimizar, processar e definir manualmente a relação entre os Bones e os vértices em suas malhas (consulte a [animação estrutural na Wikipédia](https://en.wikipedia.org/wiki/Skeletal_animation)). Ele é mais útil para fazer arquivos. x exportados por aplicativos DCC (como 3DS Max e Maya) mais amigáveis para hardware e para melhorar a velocidade de renderização de suas malhas subcapadas no modo de processamento de software.<br/> |
| [**Interface ID3DX10Sprite**](id3dx10sprite.md)               | A interface ID3DX10Sprite fornece um conjunto de métodos que simplificam o processo de desenho de sprites usando o Microsoft Direct3D.<br/>                                                                                                                                                                                                                                                                                            |
| [**Interface ID3DX10ThreadPump**](id3dx10threadpump.md)       | Usado para executar tarefas de forma assíncrona. Esse objeto ocupa uma quantidade significativa de recursos, portanto, em geral, apenas um deve ser criado por aplicativo.<br/>                                                                                                                                                                                                                                                                  |
| [**Interface ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)   | Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de D3DX](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




