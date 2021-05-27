---
title: Persistência
description: Persistência
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6cffab1c9a0f2746e57e356a90698caf9903deb
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549281"
---
# <a name="persistence"></a>Persistência

Um controle implementa uma ou mais de várias interfaces de persistência para dar suporte à persistência de seu estado. Por exemplo, a interface [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) dá suporte à persistência baseada em fluxo do estado do controle. **IPersistStreamInit** é uma substituição para [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) e adiciona um método de inicialização, [**InitNew**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew). Os outros métodos são os mesmos em ambas as interfaces. **IPersistStreamInit** não é derivado de **IPersistStream**; um objeto dá suporte a apenas uma das duas interfaces com base em se requer a capacidade de inicializar novas instâncias de si mesma.

Outras interfaces de persistência que um controle pode oferecer incluem: [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). O implementador de controle deve decidir quais tipos de persistência são mais importantes e implementar as interfaces de persistência apropriadas. O implementador de controle também decide o que salvar. Por exemplo, um controle pode salvar os valores atuais de suas propriedades ou sua localização e tamanho dentro de seu contêiner. O cliente decide qual interface prefere usar.

Antes de carregar um controle de seu estado persistente, um cliente pode verificar o \_ sinalizador OLEMISC SETCLIENTSITEFIRST para determinar se o controle dá suporte à obtenção de suas propriedades de site e de ambiente do cliente antes de carregar seu estado persistente. Essa otimização pode poupar tempo ao instanciar um controle, uma vez que o controle é liberado para ignorar seus valores persistentes em vez de carregá-los apenas para que sejam substituídos pelas propriedades de ambiente fornecidas pelo cliente.

Um controle também pode dar suporte a salvar e restaurar seu estado em um conjunto de propriedades OLE, um conjunto de identificadores e valores em um formato especificado. Esse recurso pode ser útil com contêineres como Visual Basic, que salva seus programas em um formato de texto. Um controle que deseja dar suporte a esse recurso implementa [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) e [**IDataObject::SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) para passar seus valores de propriedade para e do contêiner, respectivamente. É trabalho do contêiner converter essas informações em texto e salvá-la. Os identificadores usados pelo controle correspondem aos nomes de propriedade do controle e aos valores. Consulte a CDK do OLE para ver a definição desse conjunto de propriedades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 