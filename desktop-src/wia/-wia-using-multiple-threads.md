---
description: Ao usar uma Windows WIA (Aquisição de Imagem) em mais de um thread em um único processo, um aplicativo deve fornecer marshaling para essa interface.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Usando vários threads em um aplicativo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707adbfe6cd24152209e318bed73a0b6d7fee54b6cfa1e8fbcfecac67e272082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208002"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Usando vários threads em um aplicativo WIA

Ao usar uma Windows WIA (Aquisição de Imagem) em mais de um thread em um único processo, um aplicativo deve fornecer marshaling para essa interface. Se um thread criar um ponteiro de interface, você não poderá usar esse ponteiro em um thread diferente sem marshalling.

Por exemplo, se um thread em um aplicativo obtiver um ponteiro para a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2,**](-wia-iwiaitem2.md) um thread separado não poderá usar esse ponteiro de interface sem marshalling.

Uma técnica comum usada para realizar esse marshalling é usar a tabela de interface global. A tabela de interface global é uma tabela mantida em todos os threads em um único processo. Todos os threads em execução no processo podem recuperar interfaces que são registradas na tabela de interface global. Essa técnica evita a necessidade de criar fluxos para passar interfaces entre threads.

Para obter informações sobre como usar a tabela de interface global, consulte [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Mesmo que você não pretenda usar vários threads em um aplicativo WIA, você deve supor que todas as funções de retorno de chamada de evento de dispositivo ou transferência de dados são executados em threads separados.

 

 
