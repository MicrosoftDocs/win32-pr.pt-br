---
title: Ligação tardia do que está acontecendo nos bastidores
description: Este tópico descreve como a associação tardia funciona no ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, associação tardia, o que está acontecendo nos bastidores
- Associação de anúncio, associação tardia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454342"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Associação tardia: o que está acontecendo nos bastidores?

A lista a seguir descreve o processo geral para executar uma ligação tardia:

-   Algo é associado a um objeto de diretório ADSI. Por exemplo, "LDAP:Binding = Jeffsmith, OU = Sales, DC = Fabrikam, DC = COM" é associado usando associação tardia COM. Isso faz com que o ADSI chame o método [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) na interface **IDispatch** .
-   A ADSI localiza um objeto na classe User e cria um objeto que dá suporte às interfaces apropriadas, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   O ADSI executa uma pesquisa no registro e localiza CLSIDs de extensão para o usuário. Lembre-se de que o ADSI armazena esses dados em cache.
-   Algo faz uma chamada para o método **MyNewMethod** . A ADSI pesquisa sua ID de expedição e as IDs de expedição para outras extensões ADSI. Em seguida, o ADSI localiza a extensão que atende a essa chamada e chama a interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para essa extensão.
-   A extensão executa a função.
-   Agora, o gravador do cliente invoca o método **YourNewMethod** usando a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para a extensão atual. A implementação de **IDispatch** da extensão é delegada de volta para o **IDispatch** para ADSI.
-   O [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para ADSI procura novamente a extensão apropriada ou, em seguida, chama a extensão apropriada usando a interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para essa extensão.

 

 