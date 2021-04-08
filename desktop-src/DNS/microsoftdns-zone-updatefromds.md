---
title: Método UpdateFromDS da classe MicrosoftDNS_Zone
description: O método UpdateFromDS força uma atualização da zona do serviço de diretório (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- DNS do método UpdateFromDS
- Método UpdateFromDS DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone classe DNS, método UpdateFromDS
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086519"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="38034-106">Método UpdateFromDS da classe de \_ zona MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="38034-106">UpdateFromDS method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="38034-107">O método **UpdateFromDS** força uma atualização da zona do serviço de diretório (DS).</span><span class="sxs-lookup"><span data-stu-id="38034-107">The **UpdateFromDS** method forces an update of the zone from the Directory Service (DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="38034-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38034-108">Syntax</span></span>


```mof
void UpdateFromDS();
```



## <a name="parameters"></a><span data-ttu-id="38034-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38034-109">Parameters</span></span>

<span data-ttu-id="38034-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="38034-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38034-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38034-111">Return value</span></span>

<span data-ttu-id="38034-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="38034-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38034-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="38034-113">Remarks</span></span>

<span data-ttu-id="38034-114">Para executar esse método com êxito, o Zonetype deve ser zero e a zona deve ser armazenada no DS.</span><span class="sxs-lookup"><span data-stu-id="38034-114">In order to successfully execute this method, the ZoneType must be zero, and the zone must be stored on the DS.</span></span>

## <a name="requirements"></a><span data-ttu-id="38034-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38034-115">Requirements</span></span>



| <span data-ttu-id="38034-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="38034-116">Requirement</span></span> | <span data-ttu-id="38034-117">Valor</span><span class="sxs-lookup"><span data-stu-id="38034-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38034-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38034-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38034-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="38034-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="38034-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38034-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38034-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="38034-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="38034-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="38034-122">Namespace</span></span><br/>                | <span data-ttu-id="38034-123">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="38034-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="38034-124">MOF</span><span class="sxs-lookup"><span data-stu-id="38034-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38034-125"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38034-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38034-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="38034-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38034-127">**\_Zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="38034-128">**Método AgeAllRecords da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="38034-129">**Método ChangeZoneType da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="38034-130">**Método createzone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="38034-131">**Método ForceRefresh da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-131">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="38034-132">**Método getdistinguiname da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-132">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="38034-133">**Método PauseZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-133">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="38034-134">**Método ReloadZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-134">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="38034-135">**Método ResetSecondaries da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-135">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="38034-136">**Método ResumeZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-136">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="38034-137">**Método WriteBackZone da classe de \_ zona MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="38034-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





