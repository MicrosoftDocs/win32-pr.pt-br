---
title: Persistência
description: Persistência
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5fc0c8e389c7babdf80b76719b39fc02d5604
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008462"
---
# <a name="persistence"></a>Persistência

Um controle implementa uma ou mais de várias interfaces de persistência para dar suporte à persistência de seu estado. Por exemplo, a interface [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) dá suporte à persistência baseada em fluxo do estado do controle. **IPersistStreamInit** é uma substituição para [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) e adiciona um método de inicialização, [**InitNew**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew). Os outros métodos são os mesmos em ambas as interfaces. **IPersistStreamInit** não é derivado de **IPersistStream**; um objeto dá suporte a apenas uma das duas interfaces com base em se requer a capacidade de inicializar novas instâncias de si mesma.

Outras interfaces de persistência que um controle pode oferecer incluem: [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). O implementador de controle deve decidir quais tipos de persistência são mais importantes e implementar as interfaces de persistência apropriadas. O implementador de controle também decide o que salvar. Por exemplo, um controle pode salvar os valores atuais de suas propriedades ou sua localização e tamanho dentro de seu contêiner. O cliente decide qual interface prefere usar.

Antes de carregar um controle de seu estado persistente, um cliente pode verificar o \_ sinalizador OLEMISC SETCLIENTSITEFIRST para determinar se o controle dá suporte à obtenção de suas propriedades de site e de ambiente do cliente antes de carregar seu estado persistente. Essa otimização pode poupar tempo ao instanciar um controle, uma vez que o controle é liberado para ignorar seus valores persistentes em vez de carregá-los apenas para que sejam substituídos pelas propriedades de ambiente fornecidas pelo cliente.

Um controle também pode dar suporte a salvar e restaurar seu estado em um conjunto de propriedades OLE, um conjunto de identificadores e valores em um formato especificado. Esse recurso pode ser útil com contêineres como Visual Basic, que salva seus programas em um formato de texto. Um controle que deseja dar suporte a esse recurso implementa [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) e [**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) para passar seus valores de propriedade para e do contêiner, respectivamente. É o trabalho do contêiner para converter essas informações em texto e salvá-las. Os identificadores usados pelo controle correspondem aos nomes de Propriedade do controle e aos valores. Consulte o CDK OLE para a definição deste conjunto de propriedades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 