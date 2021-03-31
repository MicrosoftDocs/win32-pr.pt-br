---
title: Representação visual
description: Um controle dá suporte ao posicionamento e à exibição em seu contêiner por meio de tecnologia de documento composto e tecnologia de arrastar e soltar OLE que envolve o controle e seu contêiner.
ms.assetid: a7940560-360c-4c0d-9ac1-d051adb0b83e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9711dccbc7aa17f0b4a2ff228b2e2e4421e5083b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637208"
---
# <a name="visual-representation"></a>Representação visual

Um controle dá suporte ao posicionamento e à exibição em seu contêiner por meio de tecnologia de documento composto e tecnologia de arrastar e soltar OLE que envolve o controle e seu contêiner. O controle deve ser capaz de se desenhar enquanto o contêiner gerencia a posição do controle e seu tamanho.

Os controles são adicionados às funções básicas fornecidas por documentos OLE. Um controle chama o método [**IOleClientSite:: RequestNewObjectLayout**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-requestnewobjectlayout) do seu cliente para informar ao seu contêiner que ele deseja alterar seu tamanho. O cliente chama o [**IOleObject:: getextensão**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent) do controle para obter o novo tamanho e chama [**IOleInPlaceObject:: SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects) para definir o controle como seu novo tamanho.

Controles que dão suporte somente a [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) não dão suporte a cache por meio de [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2) porque o cache requer suporte para [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage). No entanto, esses controles devem fornecer uma maneira para o cliente renderizar o controle por meio de [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) para que o cliente possa, opcionalmente, criar e gerenciar seu próprio cache dos dados da apresentação para o controle.

Os controles usam o tipo HIMETRIC para suas coordenadas. No entanto, contêineres diferentes podem usar diferentes sistemas de coordenadas. O contêiner deseja receber coordenadas em seu próprio sistema, mas o controle não sabe necessariamente quais coordenadas seu contêiner está usando. Para se comunicar com êxito, o controle precisa de uma maneira de converter valores em suas coordenadas do contêiner. O contêiner fornece um objeto de site com o método [**IOleControlSite:: TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) . O controle chama esse método primeiro no site do cliente do contêiner para converter suas coordenadas nas coordenadas apropriadas para o contêiner. Em seguida, ele pode passar as coordenadas convertidas para o contêiner.

Os controles podem chamar [**IOleControlSite:: LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive) no objeto do site do contêiner para impedir que o contêiner tente rebaixar o controle do estado ativo in-loco. Rebaixar o controle dessa maneira faz com que o controle seja desativado e sua janela destruída, portanto, se o controle precisar manter sua janela por uma duração conhecida, ele poderá chamar **LockInPlaceActive** para garantir seu estado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




