---
description: Ao usar uma interface de aquisição de imagem do Windows (WIA) em mais de um thread em um único processo, um aplicativo deve fornecer marshaling para essa interface.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Usando vários threads em um aplicativo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090491"
---
# <a name="using-multiple-threads-in-a-wia-application"></a>Usando vários threads em um aplicativo WIA

Ao usar uma interface de aquisição de imagem do Windows (WIA) em mais de um thread em um único processo, um aplicativo deve fornecer marshaling para essa interface. Se um thread criar um ponteiro de interface, você não poderá usar esse ponteiro em um thread diferente sem Marshalling.

Por exemplo, se um thread em um aplicativo obtiver um ponteiro para a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) , um thread separado não poderá usar esse ponteiro de interface sem Marshalling.

Uma técnica comum usada para realizar esse marshaling é usar a tabela de interface global. A tabela de interface global é uma tabela mantida em todos os threads em um único processo. Todos os threads em execução no processo podem recuperar interfaces registradas para a tabela de interface global. Essa técnica evita a necessidade de criar fluxos para passar interfaces entre threads.

Para obter informações sobre como usar a tabela de interface global, consulte [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Mesmo que você não pretenda usar vários threads em um aplicativo WIA, você deve pressupor que todas as funções de transferência de dados ou de retorno de chamada de evento de dispositivo sejam executadas em threads separados.

 

 
