---
title: Objeto de fonte padrão
description: Objeto de fonte padrão
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0fbe2509dd85c1d15b40dc8008dba60d948b5c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008402"
---
# <a name="standard-font-object"></a>Objeto de fonte padrão

A propriedade de fonte de ambiente padrão fornecida pelo contêiner e a propriedade de fonte padrão fornecida pelo controle fornecem um objeto de fonte padrão. Ou seja, essas fontes padrão fornecem um ponteiro **IDispatch** para um objeto Font padrão.

O objeto Font é uma implementação fornecida pelo sistema de um conjunto de interfaces sobre o suporte à fonte de GDI subjacente. Um objeto de fonte é criado por meio da função de API [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) dada uma estrutura [**FONTDESC**](/windows/win32/api/olectl/ns-olectl-fontdesc) . O objeto Font dá suporte a várias propriedades de leitura/gravação, bem como a métodos personalizados por meio de sua interface [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)e dá suporte ao mesmo conjunto de Propriedades (mas não aos métodos) por meio de um [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)de dispinterface. A dispinterface é usada para as propriedades de fonte mencionadas anteriormente. As propriedades correspondem aos atributos de fonte GDI descritos na estrutura [**LOGFONT**](/windows/win32/api/dimm/ns-dimm-logfonta) .

O objeto Font também dá suporte à interface de saída [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que um cliente possa determinar quando as propriedades da fonte são alteradas. Como o objeto Font dá suporte a pelo menos uma interface de saída, ele também implementa [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) e um ponto de conexão para **IPropertyNotifySink** para essa finalidade.

O objeto Font fornece uma propriedade hFont que é uma alça de fonte do Windows que está em conformidade com os outros atributos especificados para a fonte. O objeto Font atrasa a obtenção dessa fonte quando possível, portanto, configurando consecutivamente duas propriedades em uma fonte não fará com que uma fonte intermediária seja realizada. Além disso, como uma otimização, o objeto de fonte padrão mantém um cache de identificadores de fonte. Dois objetos Font no mesmo processo que têm propriedades idênticas retornarão o mesmo identificador de fonte. O objeto Font pode remover fontes desse cache no, o que introduz considerações especiais para clientes que usam essa propriedade hFont. Consulte [**IFont:: get \_ hFont**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) para obter mais detalhes.

O objeto Font também dá suporte a [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , de modo que ele pode salvar e carregar a si mesmo de uma instância de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Qualquer outro objeto que usa um objeto de fonte internamente normalmente salvaria e carregaria a fonte como parte da própria manipulação de persistência do objeto.

Além disso, o objeto Font dá suporte a [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) por meio do qual ele fornece um conjunto de propriedades que contém valores tipados para cada propriedade Font.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle](control-properties.md)
</dt> </dl>

 

 