---
title: Persistência
description: Persistência
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c8600307bfe6c29f72fb9d29e633358062c4e8c1c61da8898173cf190f1d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500326"
---
# <a name="persistence"></a>Persistência

Um controle implementa uma ou mais das várias interfaces de persistência para dar suporte à persistência de seu estado. Por exemplo, a interface [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) dá suporte à persistência baseada em fluxo do estado do controle. **IPersistStreamInit** é uma substituição para [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) e adiciona um método de inicialização, [**InitNew.**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew) Os outros métodos são os mesmos em ambas as interfaces. **IPersistStreamInit** não é derivado de **IPersistStream**; um objeto dá suporte a apenas uma das duas interfaces com base em se ele requer a capacidade de inicializar novas instâncias de si mesmo.

Outras interfaces de persistência que um controle pode oferecer incluem: [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistMemory,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [**IPersistPropertyBag,**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). O implementador de controle deve decidir quais tipos de persistência são mais importantes e implementar as interfaces de persistência apropriadas. O implementador de controle também decide o que salvar. Por exemplo, um controle pode salvar os valores atuais de suas propriedades ou seu local e tamanho em seu contêiner. O cliente decide qual interface ele prefere usar.

Antes de carregar um controle de seu estado persistente, um cliente pode verificar o sinalizador SETCLIENTSITEFIRST OLEMISC para determinar se o controle dá suporte à obter suas propriedades de site e ambiente do cliente antes de carregar seu estado \_ persistente. Essa otimização pode economizar tempo ao inciar um controle, pois o controle é livre para ignorar seus valores persistentes em vez de carregá-los apenas para que eles os substituim pelas propriedades de ambiente fornecidas pelo cliente.

Um controle também pode dar suporte a salvar e restaurar seu estado em um conjunto de propriedades OLE, um conjunto de identificadores e valores em um formato especificado. Esse recurso pode ser útil com contêineres como Visual Basic, que salva seus programas em um formato textual. Um controle que deseja dar suporte a esse recurso implementa [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) e [**IDataObject::SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) para passar seus valores de propriedade para e do contêiner, respectivamente. É trabalho do contêiner converter essas informações em texto e salvá-la. Os identificadores usados pelo controle correspondem aos nomes de propriedade do controle e aos valores. Consulte a CDK do OLE para ver a definição desse conjunto de propriedades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ActiveX Controles](activex-controls.md)
</dt> </dl>

 

 