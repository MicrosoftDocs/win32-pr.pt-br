---
title: AuthenticationLevel
description: Define o nível de autenticação para aplicativos que não chamam CoInitializeSecurity ou para aplicativos que chamam CoInitializeSecurity e especificam uma AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- COM valor do registro AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292848"
---
# <a name="authenticationlevel"></a><span data-ttu-id="cb2e7-104">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="cb2e7-104">AuthenticationLevel</span></span>

<span data-ttu-id="cb2e7-105">Define o nível de autenticação para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou para aplicativos que chamam **CoInitializeSecurity** e especificam uma AppID.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-105">Sets the authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or for applications that call **CoInitializeSecurity** and specify an AppID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="cb2e7-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="cb2e7-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="cb2e7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb2e7-107">Remarks</span></span>

<span data-ttu-id="cb2e7-108">Esse é um valor de **reg \_ DWORD** equivalente às \_ constantes de nível de \_ autenticação RPC C \_ .</span><span class="sxs-lookup"><span data-stu-id="cb2e7-108">This is a **REG\_DWORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="cb2e7-109">Valor</span><span class="sxs-lookup"><span data-stu-id="cb2e7-109">Value</span></span> | <span data-ttu-id="cb2e7-110">Constante</span><span class="sxs-lookup"><span data-stu-id="cb2e7-110">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="cb2e7-111">1</span><span class="sxs-lookup"><span data-stu-id="cb2e7-111">1</span></span>     | <span data-ttu-id="cb2e7-112">RPC \_ C \_ Authn \_ nível \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="cb2e7-112">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="cb2e7-113">2</span><span class="sxs-lookup"><span data-stu-id="cb2e7-113">2</span></span>     | <span data-ttu-id="cb2e7-114">\_conexão em \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="cb2e7-114">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="cb2e7-115">3</span><span class="sxs-lookup"><span data-stu-id="cb2e7-115">3</span></span>     | <span data-ttu-id="cb2e7-116">\_chamada de \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="cb2e7-116">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="cb2e7-117">4</span><span class="sxs-lookup"><span data-stu-id="cb2e7-117">4</span></span>     | <span data-ttu-id="cb2e7-118">\_PCT do \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="cb2e7-118">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="cb2e7-119">5</span><span class="sxs-lookup"><span data-stu-id="cb2e7-119">5</span></span>     | <span data-ttu-id="cb2e7-120">\_integridade de \_ pkt do \_ nível \_ de \_ autenticação RPC C</span><span class="sxs-lookup"><span data-stu-id="cb2e7-120">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="cb2e7-121">6</span><span class="sxs-lookup"><span data-stu-id="cb2e7-121">6</span></span>     | <span data-ttu-id="cb2e7-122">\_privacidade do \_ PCT do \_ nível \_ de \_ autenticação RPC C</span><span class="sxs-lookup"><span data-stu-id="cb2e7-122">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="cb2e7-123">O valor de **AuthenticationLevel** é semelhante ao valor de [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="cb2e7-123">The **AuthenticationLevel** value is similar to the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) value.</span></span> <span data-ttu-id="cb2e7-124">Se o valor de **AuthenticationLevel** estiver presente, ele será usado em vez do valor de **LegacyAuthenticationLevel** para esse AppID.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-124">If the **AuthenticationLevel** value is present, it is used instead of the **LegacyAuthenticationLevel** value for that AppID.</span></span>

<span data-ttu-id="cb2e7-125">Se o valor de **AuthenticationLevel** for do tipo incorreto ou fora do intervalo, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) falhará, causando falha no marshaling da interface.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-125">If the **AuthenticationLevel** value is of the wrong type or out of range, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fails, causing interface marshaling to fail.</span></span> <span data-ttu-id="cb2e7-126">Isso impede que o aplicativo faça qualquer chamada (entre apartamento, entre threads, entre processos ou entre computadores).</span><span class="sxs-lookup"><span data-stu-id="cb2e7-126">This prevents the application from making any calls at all (cross-apartment, cross-thread, cross-process, or cross-computer).</span></span>

<span data-ttu-id="cb2e7-127">Os valores **AuthenticationLevel** e [**AccessPermission**](accesspermission.md) são independentes.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-127">The **AuthenticationLevel** and [**AccessPermission**](accesspermission.md) values are independent.</span></span> <span data-ttu-id="cb2e7-128">Se um não estiver presente, o padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="cb2e7-128">If one is not present, the default is used.</span></span> <span data-ttu-id="cb2e7-129">As regras a seguir listam a interação entre o valor **AuthenticationLevel** e o valor **AccessPermission** :</span><span class="sxs-lookup"><span data-stu-id="cb2e7-129">The following rules list the interaction between the **AuthenticationLevel** value and the **AccessPermission** value:</span></span>

-   <span data-ttu-id="cb2e7-130">Se **AuthenticationLevel** for None, os valores [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) serão ignorados (para esse aplicativo).</span><span class="sxs-lookup"><span data-stu-id="cb2e7-130">If the **AuthenticationLevel** is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>
-   <span data-ttu-id="cb2e7-131">Se o **AuthenticationLevel** não estiver presente e [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) for None, os valores [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) serão ignorados (para esse aplicativo).</span><span class="sxs-lookup"><span data-stu-id="cb2e7-131">If the **AuthenticationLevel** is not present and the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb2e7-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb2e7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb2e7-133">Constantes de nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="cb2e7-133">Authentication Level Constants</span></span>](com-authentication-level-constants.md)
</dt> <dt>

[<span data-ttu-id="cb2e7-134">**LegacyAuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="cb2e7-134">**LegacyAuthenticationLevel**</span></span>](legacyauthenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="cb2e7-135">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="cb2e7-135">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="cb2e7-136">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="cb2e7-136">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




