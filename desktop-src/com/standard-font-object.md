---
title: Objeto de fonte padrão
description: Objeto de fonte padrão
ms.assetid: f9b54dc4-24d4-4eb7-b43f-c481d64e52df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1beb4ac2890cd3314c1b23f847192f1d3248b02e301c27d5990f524c74c0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104149"
---
# <a name="standard-font-object"></a>Objeto de fonte padrão

A propriedade de fonte ambiente padrão fornecida pelo contêiner e a propriedade de fonte padrão fornecida pelo controle fornecem um objeto de fonte padrão. Ou seja, essas fontes padrão fornecem um ponteiro **IDispatch** para um objeto de fonte padrão.

O objeto de fonte é uma implementação fornecida pelo sistema de um conjunto de interfaces sobre o suporte à fonte GDI subjacente. Um objeto de fonte é criado por meio da função de API [**OleCreateFontIndirect dada**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect) uma [**estrutura FONTDESC.**](/windows/win32/api/olectl/ns-olectl-fontdesc) O objeto de fonte dá suporte a várias propriedades de leitura/gravação, bem como métodos personalizados por meio de sua interface [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)e dá suporte ao mesmo conjunto de propriedades (mas não os métodos) por meio de um [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)dispinterface. A dispinterface é usada para as propriedades de fonte mencionadas anteriormente. As propriedades correspondem aos atributos de fonte GDI descritos na [**estrutura LOGFONT.**](/windows/win32/api/dimm/ns-dimm-logfonta)

O objeto de fonte também dá suporte à interface de saída [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que um cliente possa determinar quando as propriedades da fonte mudam. Como o objeto de fonte dá suporte a pelo menos uma interface de saída, ele também implementa [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) e um ponto de conexão para **IPropertyNotifySink** para essa finalidade.

O objeto de fonte fornece uma propriedade hFont que é um identificador Windows fonte que está em conformidade com os outros atributos especificados para a fonte. O objeto de fonte atrasa a realização dessa fonte quando possível, portanto, definir duas propriedades consecutivamente em uma fonte não causará a realização de uma fonte intermediária. Além disso, como uma otimização, o objeto de fonte padrão mantém um cache de identificador de fonte. Dois objetos de fonte no mesmo processo que têm propriedades idênticas retornarão o mesmo alça de fonte. O objeto de fonte pode remover fontes desse cache à vontade, o que apresenta considerações especiais para clientes que usam essa propriedade hFont. Consulte [**IFont::get \_ hFont**](/windows/desktop/api/OCIdl/nf-ocidl-ifont-get_hfont) para obter mais detalhes.

O objeto de fonte também dá [**suporte a IPersistStream,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) de forma que ele possa salvar e carregar a si mesmo de uma instância do [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Qualquer outro objeto que usa um objeto de fonte internamente normalmente salvaria e carregaria a fonte como parte do próprio tratamento de persistência do objeto.

Além disso, o objeto de fonte dá suporte a [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) por meio do qual ele fornece um conjunto de propriedades que contém valores digitados para cada propriedade de fonte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle](control-properties.md)
</dt> </dl>

 

 