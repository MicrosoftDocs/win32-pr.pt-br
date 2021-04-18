---
title: LegacyImpersonationLevel
description: Define o nível padrão de representação para aplicativos que não chamam CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- COM valor do registro LegacyImpersonationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810837"
---
# <a name="legacyimpersonationlevel"></a><span data-ttu-id="03f57-104">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="03f57-104">LegacyImpersonationLevel</span></span>

<span data-ttu-id="03f57-105">Define o nível padrão de representação para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="03f57-105">Sets the default level of impersonation for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="03f57-106">Não é recomendável que você altere esse valor, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="03f57-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="03f57-107">Se você estiver alterando esse valor para afetar as configurações de segurança para um aplicativo COM específico, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico.</span><span class="sxs-lookup"><span data-stu-id="03f57-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="03f57-108">Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="03f57-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="03f57-109">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="03f57-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="03f57-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="03f57-110">Remarks</span></span>

<span data-ttu-id="03f57-111">Esse é um valor de **reg \_ Word** equivalente às constantes de nível de imp da RPC \_ C \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="03f57-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_IMP\_LEVEL constants.</span></span>



| <span data-ttu-id="03f57-112">Valor</span><span class="sxs-lookup"><span data-stu-id="03f57-112">Value</span></span> | <span data-ttu-id="03f57-113">Constante</span><span class="sxs-lookup"><span data-stu-id="03f57-113">Constant</span></span>                        |
|-------|---------------------------------|
| <span data-ttu-id="03f57-114">1</span><span class="sxs-lookup"><span data-stu-id="03f57-114">1</span></span>     | <span data-ttu-id="03f57-115">nível de imp do RPC \_ C- \_ \_ \_ anônimo</span><span class="sxs-lookup"><span data-stu-id="03f57-115">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   |
| <span data-ttu-id="03f57-116">2</span><span class="sxs-lookup"><span data-stu-id="03f57-116">2</span></span>     | <span data-ttu-id="03f57-117">\_identificação de \_ nível de imp \_ \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="03f57-117">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    |
| <span data-ttu-id="03f57-118">3</span><span class="sxs-lookup"><span data-stu-id="03f57-118">3</span></span>     | <span data-ttu-id="03f57-119">\_representação de \_ nível de imp \_ \_ do RPC C</span><span class="sxs-lookup"><span data-stu-id="03f57-119">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> |
| <span data-ttu-id="03f57-120">4</span><span class="sxs-lookup"><span data-stu-id="03f57-120">4</span></span>     | <span data-ttu-id="03f57-121">\_delegado de \_ nível de imp \_ \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="03f57-121">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    |



 

<span data-ttu-id="03f57-122">Se esse valor de registro não estiver presente, o nível de representação padrão estabelecido pelo sistema será 2 (a identificação do nível de imp do RPC \_ C \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="03f57-122">If this registry value is not present, the default impersonation level established by the system is 2 (RPC\_C\_IMP\_LEVEL\_IDENTIFY).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03f57-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03f57-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03f57-124">Registrando servidores COM</span><span class="sxs-lookup"><span data-stu-id="03f57-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="03f57-125">Definindo a segurança de todo o processo</span><span class="sxs-lookup"><span data-stu-id="03f57-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




