---
title: Método StopService da classe MicrosoftDNS_Server
description: O método StopService interrompe o servidor DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- DNS do método StopService
- Método StopService DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de classe de DNS, método StopService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455330"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="6a58b-106">Método StopService da classe de \_ servidor MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="6a58b-106">StopService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="6a58b-107">O método **StopService** interrompe o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="6a58b-107">The **StopService** method stops the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a58b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a58b-108">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="6a58b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a58b-109">Parameters</span></span>

<span data-ttu-id="6a58b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6a58b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a58b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a58b-111">Return value</span></span>

<span data-ttu-id="6a58b-112">\_O êxito do erro indica que o serviço foi interrompido com êxito.</span><span class="sxs-lookup"><span data-stu-id="6a58b-112">ERROR\_SUCCESS indicates the service was successfully stopped.</span></span> <span data-ttu-id="6a58b-113">Qualquer outro valor é um código de erro.</span><span class="sxs-lookup"><span data-stu-id="6a58b-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a58b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a58b-114">Requirements</span></span>



| <span data-ttu-id="6a58b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a58b-115">Requirement</span></span> | <span data-ttu-id="6a58b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6a58b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a58b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a58b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a58b-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6a58b-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6a58b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a58b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a58b-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a58b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6a58b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a58b-121">Namespace</span></span><br/>                | <span data-ttu-id="6a58b-122">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="6a58b-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6a58b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6a58b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a58b-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a58b-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a58b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a58b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a58b-126">**\_Servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6a58b-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="6a58b-127">**Método StartService da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6a58b-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="6a58b-128">**Método StartScavenging da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6a58b-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="6a58b-129">**Método getdistinguiname da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6a58b-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





