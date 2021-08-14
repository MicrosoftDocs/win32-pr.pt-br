---
description: Esta seção contém informações de referência para as interfaces COM (component object model) fornecidas pela biblioteca de utilitários D3DX em Elementos Gráficos do Direct3D 10.
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: Interfaces D3DX (elementos gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65edec72206540d1f0c8e91e8a375daf3844f3703d2f05a3b844697230b300e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304218"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a>Interfaces D3DX (elementos gráficos do Direct3D 10)

Esta seção contém informações de referência para as interfaces COM (modelo de objeto de componente) fornecidas pela biblioteca de utilitários D3DX. As interfaces a seguir são usadas com a biblioteca de utilitários D3DX.



| Interfaces                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)       | Objeto de carregamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para carregar dados de forma assíncrona.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md) | Objeto de processamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para processar dados carregados de forma assíncrona.<br/>                                                                                                                                                                                                                                                                                      |
| [**ID3DX10Font Interface**](id3dx10font.md)                   | A interface ID3DX10Font encapsula as texturas e os recursos necessários para renderizar uma fonte específica em um dispositivo específico.<br/>                                                                                                                                                                                                                                                                                                |
| [**ID3DX10Mesh Interface**](id3dx10mesh.md)                   | Os aplicativos usam os métodos da interface ID3DX10Mesh para manipular objetos de malha.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**ID3DX10MeshBuffer Interface**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md)           | ID3DX10SkinInfo permite otimizar, processar e definir manualmente a relação entre o urso e os vértices em suas malhas (consulte Animaçãokeletal na [Wikipédia).](https://en.wikipedia.org/wiki/Skeletal_animation) Ele é mais útil para tornar os arquivos .x exportados por Aplicativos DCC (como o 3DS Max e Maya) mais amigáveis com hardware e para melhorar a velocidade de renderização de suas malhas desmistreladas no modo de renderização de software.<br/> |
| [**ID3DX10Sprite Interface**](id3dx10sprite.md)               | A interface ID3DX10Sprite fornece um conjunto de métodos que simplificam o processo de desenho de sprites usando o Microsoft Direct3D.<br/>                                                                                                                                                                                                                                                                                            |
| [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)       | Usado para executar tarefas de forma assíncrona. Esse objeto ocupa uma quantidade substancial de recursos, portanto, geralmente, apenas um deve ser criado por aplicativo.<br/>                                                                                                                                                                                                                                                                  |
| [**ID3DXMatrixStack Interface**](d3d10-id3dxmatrixstack.md)   | Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matrizes.<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de D3DX](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




