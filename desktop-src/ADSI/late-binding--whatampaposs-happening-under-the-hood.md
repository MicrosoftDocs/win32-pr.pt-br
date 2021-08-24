---
title: Associação tardia do que está acontecendo nos hood
description: Este tópico descreve como a associação tardia funciona no ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- extensões ADSI, associação tardia, o que está acontecendo nos hood
- associação do AD, associação tardia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c479472a2974f31e8ecdd4308b01cf7c7251eada3f907d5d90ecf152028399b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637886"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Associação tardia: o que está acontecendo nos hood?

A lista a seguir descreve o processo geral para executar uma vinculação tardia:

-   Algo se vincula a um objeto de diretório ADSI. Por exemplo, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" é vinculado usando associação tardia COM. Isso faz com que a ADSI chame [**o método QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) na interface **IDispatch.**
-   ADSI localiza um objeto na classe de usuário e cria um objeto que dá suporte às interfaces apropriadas, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   A ADSI executa uma pesquisa no Registro e localiza CLSIDs de extensão para o usuário. Esteja ciente de que a ADSI armazena esses dados em cache.
-   Algo faz uma chamada para o **método MyNewMethod.** A ADSI pesquisa sua ID de expedição e as IDs de expedição para outras extensões ADSI. A ADSI localiza a extensão que atende a essa chamada e chama a interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para essa extensão.
-   A extensão executa a função .
-   Agora, o autor do cliente invoca o **método YourNewMethod** usando a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para a extensão atual. A implementação de **IDispatch** da extensão delega de volta ao **IDispatch** para ADSI.
-   O [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para ADSI pesquisa novamente a extensão apropriada ou a si mesmo, em seguida, chama a extensão apropriada usando a interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para essa extensão.

 

 