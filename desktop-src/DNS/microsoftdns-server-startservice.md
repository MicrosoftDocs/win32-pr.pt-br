---
title: Método StartService da classe MicrosoftDNS_Server
description: O método StartService inicia o servidor DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- Método StartService DNS
- Método StartService DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de classe de DNS, método StartService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762737"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="eaef4-106">Método StartService da classe de \_ servidor MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="eaef4-106">StartService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="eaef4-107">O método **StartService** inicia o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="eaef4-107">The **StartService** method starts the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaef4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaef4-108">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="eaef4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaef4-109">Parameters</span></span>

<span data-ttu-id="eaef4-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="eaef4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eaef4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eaef4-111">Return value</span></span>

<span data-ttu-id="eaef4-112">\_O êxito do erro indica que o serviço foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="eaef4-112">ERROR\_SUCCESS indicates the service was successfully started.</span></span> <span data-ttu-id="eaef4-113">Qualquer outro valor é um código de erro.</span><span class="sxs-lookup"><span data-stu-id="eaef4-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaef4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaef4-114">Requirements</span></span>



| <span data-ttu-id="eaef4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaef4-115">Requirement</span></span> | <span data-ttu-id="eaef4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="eaef4-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaef4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaef4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eaef4-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eaef4-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eaef4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaef4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eaef4-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eaef4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eaef4-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="eaef4-121">Namespace</span></span><br/>                | <span data-ttu-id="eaef4-122">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="eaef4-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="eaef4-123">MOF</span><span class="sxs-lookup"><span data-stu-id="eaef4-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaef4-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaef4-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaef4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaef4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaef4-126">**\_Servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaef4-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="eaef4-127">**Método StopService da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaef4-127">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="eaef4-128">**Método StartScavenging da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaef4-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="eaef4-129">**Método getdistinguiname da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="eaef4-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





