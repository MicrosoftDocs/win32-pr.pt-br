---
title: Objeto de imagem padrão
description: Objeto de imagem padrão
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4b74daa4f62791c12927eba3fd0472ed2a956d4b84c03e3cc373c44e12ce25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129758"
---
# <a name="standard-picture-object"></a>Objeto de imagem padrão

O objeto de imagem padrão fornece uma abstração neutra de idioma para imagens GDI: bitmaps, ícones, metaarquivos e metaarquivos aprimorados. Assim como acontece com o objeto de fonte padrão, o sistema fornece uma implementação padrão desse objeto. Suas interfaces primárias são [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), a última deriva de **IDispatch** para fornecer acesso às propriedades da imagem por meio da automação OLE. Um objeto de imagem é criado com [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).

O objeto Picture também dá suporte à interface de saída [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que um cliente possa determinar quando as propriedades da imagem são alteradas. Da mesma forma, o objeto Picture também dá suporte a [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) e a um ponto de conexão para **IPropertyNotifySink**.

O objeto Picture também dá suporte a [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , de modo que ele pode salvar e carregar a si mesmo de uma instância de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Um objeto que usa um objeto de imagem internamente normalmente salva e carrega a imagem como parte da própria manipulação de persistência do objeto. A função [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) simplifica a criação de um objeto de imagem com base no conteúdo do fluxo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle](control-properties.md)
</dt> </dl>

 

 