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
# <a name="remoteservername"></a><span data-ttu-id="4f5c0-104">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="4f5c0-104">RemoteServerName</span></span>

<span data-ttu-id="4f5c0-105">Configura o cliente para solicitar que o objeto seja executado em um determinado computador sempre que uma função de ativação é chamada para a qual uma estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) não é especificada.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-105">Configures the client to request the object be run at a particular computer whenever an activation function is called for which a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure is not specified.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4f5c0-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="4f5c0-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a><span data-ttu-id="4f5c0-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f5c0-107">Remarks</span></span>

<span data-ttu-id="4f5c0-108">O **RemoteServerName** permite o gerenciamento simples de configuração de aplicativos cliente; Eles podem ser gravados sem nomes de servidor embutidos em código e podem ser configurados modificando os valores do registro **RemoteServerName** das classes de objetos que usam.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-108">**RemoteServerName** allows simple configuration management of client applications; they may be written without hard-coded server names and can be configured by modifying the **RemoteServerName** registry values of the classes of objects they use.</span></span>

<span data-ttu-id="4f5c0-109">Conforme descrito na documentação da enumeração [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) e da estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , um dos parâmetros da ativação com distribuída é um ponteiro para uma estrutura **COSERVERINFO** .</span><span class="sxs-lookup"><span data-stu-id="4f5c0-109">As described in the documentation for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration and the [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, one of the parameters of the distributed COM activation is a pointer to a **COSERVERINFO** structure.</span></span> <span data-ttu-id="4f5c0-110">Quando esse valor não é **nulo**, as informações na estrutura **COSERVERINFO** substituem a configuração da chave **RemoteServerName** para a chamada de função.</span><span class="sxs-lookup"><span data-stu-id="4f5c0-110">When this value is not **NULL**, the information in the **COSERVERINFO** structure overrides the setting of the **RemoteServerName** key for the function call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f5c0-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f5c0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f5c0-112">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="4f5c0-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 