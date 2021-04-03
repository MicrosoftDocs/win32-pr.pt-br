---
title: LegacyAuthenticationLevel
description: Define o nível de autenticação padrão para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- COM valor do registro LegacyAuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006168"
---
# <a name="legacyauthenticationlevel"></a><span data-ttu-id="11c27-104">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="11c27-104">LegacyAuthenticationLevel</span></span>

<span data-ttu-id="11c27-105">Define o nível de autenticação padrão para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="11c27-105">Sets the default authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="11c27-106">Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="11c27-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="11c27-107">Se você estiver alterando esse valor para afetar as configurações de segurança para um aplicativo COM específico, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico.</span><span class="sxs-lookup"><span data-stu-id="11c27-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="11c27-108">Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="11c27-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="11c27-109">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="11c27-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="11c27-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="11c27-110">Remarks</span></span>

<span data-ttu-id="11c27-111">Esse é um valor de **reg \_ Word** equivalente às \_ constantes de nível de \_ autenticação RPC C \_ .</span><span class="sxs-lookup"><span data-stu-id="11c27-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="11c27-112">Valor</span><span class="sxs-lookup"><span data-stu-id="11c27-112">Value</span></span> | <span data-ttu-id="11c27-113">Constante</span><span class="sxs-lookup"><span data-stu-id="11c27-113">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="11c27-114">1</span><span class="sxs-lookup"><span data-stu-id="11c27-114">1</span></span>     | <span data-ttu-id="11c27-115">RPC \_ C \_ Authn \_ nível \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="11c27-115">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="11c27-116">2</span><span class="sxs-lookup"><span data-stu-id="11c27-116">2</span></span>     | <span data-ttu-id="11c27-117">\_conexão em \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="11c27-117">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="11c27-118">3</span><span class="sxs-lookup"><span data-stu-id="11c27-118">3</span></span>     | <span data-ttu-id="11c27-119">\_chamada de \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="11c27-119">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="11c27-120">4</span><span class="sxs-lookup"><span data-stu-id="11c27-120">4</span></span>     | <span data-ttu-id="11c27-121">\_PCT do \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="11c27-121">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="11c27-122">5</span><span class="sxs-lookup"><span data-stu-id="11c27-122">5</span></span>     | <span data-ttu-id="11c27-123">\_integridade de \_ pkt do \_ nível \_ de \_ autenticação RPC C</span><span class="sxs-lookup"><span data-stu-id="11c27-123">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="11c27-124">6</span><span class="sxs-lookup"><span data-stu-id="11c27-124">6</span></span>     | <span data-ttu-id="11c27-125">\_privacidade do \_ PCT do \_ nível \_ de \_ autenticação RPC C</span><span class="sxs-lookup"><span data-stu-id="11c27-125">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="11c27-126">Se esse valor de registro não estiver presente, o nível de autenticação padrão estabelecido pelo sistema será 2 (RPC \_ C \_ Authn \_ Connect).</span><span class="sxs-lookup"><span data-stu-id="11c27-126">If this registry value is not present, the default authentication level established by the system is 2 (RPC\_C\_AUTHN\_CONNECT).</span></span>

## <a name="related-topics"></a><span data-ttu-id="11c27-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11c27-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11c27-128">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="11c27-128">**AuthenticationLevel**</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="11c27-129">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="11c27-129">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="11c27-130">Definindo a segurança de todo o processo</span><span class="sxs-lookup"><span data-stu-id="11c27-130">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




