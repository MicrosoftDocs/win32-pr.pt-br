---
title: RemoteServerName
description: Configura o cliente para solicitar que o objeto seja executado em um determinado computador sempre que uma função de ativação é chamada para a qual uma estrutura COSERVERINFO não é especificada.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- COM valor do registro RemoteServerName COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105813713"
---
# <a name="remoteservername"></a>RemoteServerName

Configura o cliente para solicitar que o objeto seja executado em um determinado computador sempre que uma função de ativação é chamada para a qual uma estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) não é especificada.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a>Comentários

O **RemoteServerName** permite o gerenciamento simples de configuração de aplicativos cliente; Eles podem ser gravados sem nomes de servidor embutidos em código e podem ser configurados modificando os valores do registro **RemoteServerName** das classes de objetos que usam.

Conforme descrito na documentação da enumeração [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) e da estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , um dos parâmetros da ativação com distribuída é um ponteiro para uma estrutura **COSERVERINFO** . Quando esse valor não é **nulo**, as informações na estrutura **COSERVERINFO** substituem a configuração da chave **RemoteServerName** para a chamada de função.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> </dl>

 

 