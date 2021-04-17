---
title: Método ForceRefresh da classe MicrosoftDNS_Zone
description: O método ForceRefresh força uma atualização do servidor DNS secundário do servidor mestre.
ms.assetid: 8dde1703-53c3-4d1e-bfb3-f6d5d1666740
keywords:
- DNS do método ForceRefresh
- Método ForceRefresh DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone classe DNS, método ForceRefresh
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ForceRefresh
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85390230b0a0852ee479bc8b7e396972f6e69080
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105755414"
---
# <a name="forcerefresh-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="c2e6a-106">Método ForceRefresh da classe de \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c2e6a-106">ForceRefresh method of the MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="c2e6a-107">Este artigo contém referências ao termo servidor mestre, um termo que a Microsoft não usa mais.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-107">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="c2e6a-108">Quando o termo for removido do software, também o removeremos deste artigo.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-108">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="c2e6a-109">O método **ForceRefresh** força uma atualização do servidor DNS secundário do servidor mestre.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-109">The **ForceRefresh** method forces an update of the secondary DNS Server from the master server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e6a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2e6a-110">Syntax</span></span>


```mof
void ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="c2e6a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2e6a-111">Parameters</span></span>

<span data-ttu-id="c2e6a-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2e6a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2e6a-113">Return value</span></span>

<span data-ttu-id="c2e6a-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c2e6a-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e6a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e6a-115">Requirements</span></span>



| <span data-ttu-id="c2e6a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e6a-116">Requirement</span></span> | <span data-ttu-id="c2e6a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c2e6a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e6a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2e6a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e6a-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c2e6a-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c2e6a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2e6a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e6a-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2e6a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2e6a-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2e6a-122">Namespace</span></span><br/>                | <span data-ttu-id="c2e6a-123">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="c2e6a-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c2e6a-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c2e6a-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2e6a-125"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2e6a-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e6a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2e6a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e6a-127">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-128">**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-129">**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-130">**Método createzone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-131">**Método getdistinguiname da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-131">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-132">**Método PauseZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-132">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-133">**Método ReloadZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-133">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-134">**Método ResetSecondaries da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-134">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-135">**Método ResumeZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-135">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-136">**Método UpdateFromDS da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-136">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="c2e6a-137">**Método WriteBackZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2e6a-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





