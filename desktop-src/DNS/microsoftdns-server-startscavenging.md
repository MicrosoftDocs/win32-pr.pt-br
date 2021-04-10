---
title: Método StartScavenging da classe MicrosoftDNS_Server
description: O método StartScavenging inicia a eliminação de registros obsoletos nas zonas sujeitas à eliminação.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- DNS do método StartScavenging
- Método StartScavenging DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server classe DNS, método StartScavenging
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918599"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="faaba-106">Método StartScavenging da classe de \_ servidor MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="faaba-106">StartScavenging method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="faaba-107">O método **StartScavenging** inicia a eliminação de registros obsoletos nas zonas sujeitas à eliminação.</span><span class="sxs-lookup"><span data-stu-id="faaba-107">The **StartScavenging** method starts scavenging stale records in the zones subjected to scavenging.</span></span>

## <a name="syntax"></a><span data-ttu-id="faaba-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="faaba-108">Syntax</span></span>


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a><span data-ttu-id="faaba-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faaba-109">Parameters</span></span>

<span data-ttu-id="faaba-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="faaba-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="faaba-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="faaba-111">Return value</span></span>

<span data-ttu-id="faaba-112">\_O êxito do erro indica que a limpeza foi iniciada com êxito.</span><span class="sxs-lookup"><span data-stu-id="faaba-112">ERROR\_SUCCESS indicates the scavenging was successfully started.</span></span> <span data-ttu-id="faaba-113">Qualquer outro valor é um código de erro.</span><span class="sxs-lookup"><span data-stu-id="faaba-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="faaba-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faaba-114">Requirements</span></span>



| <span data-ttu-id="faaba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="faaba-115">Requirement</span></span> | <span data-ttu-id="faaba-116">Valor</span><span class="sxs-lookup"><span data-stu-id="faaba-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="faaba-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faaba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="faaba-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="faaba-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="faaba-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faaba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="faaba-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="faaba-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="faaba-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="faaba-121">Namespace</span></span><br/>                | <span data-ttu-id="faaba-122">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="faaba-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="faaba-123">MOF</span><span class="sxs-lookup"><span data-stu-id="faaba-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faaba-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faaba-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faaba-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="faaba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faaba-126">**\_Servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faaba-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="faaba-127">**Método StartService da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faaba-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="faaba-128">**Método StopService da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faaba-128">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="faaba-129">**Método getdistinguiname da classe de \_ servidor MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="faaba-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





