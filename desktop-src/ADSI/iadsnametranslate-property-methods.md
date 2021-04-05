---
title: Métodos de propriedade IADsNameTranslate (IADs. h)
description: Define a propriedade ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsNameTranslate
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918888"
---
# <a name="iadsnametranslate-property-methods"></a><span data-ttu-id="b501c-104">Métodos de propriedade IADsNameTranslate</span><span class="sxs-lookup"><span data-stu-id="b501c-104">IADsNameTranslate Property Methods</span></span>

<span data-ttu-id="b501c-105">O método Property da interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) define a propriedade **ChaseReferral** .</span><span class="sxs-lookup"><span data-stu-id="b501c-105">The property method of the [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface sets the **ChaseReferral** property.</span></span> <span data-ttu-id="b501c-106">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b501c-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b501c-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b501c-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b501c-108">**ChaseReferral**</span><span class="sxs-lookup"><span data-stu-id="b501c-108">**ChaseReferral**</span></span>
<span data-ttu-id="b501c-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b501c-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="b501c-110">Opções de busca de referência conforme definido em [**anúncios \_ Chase \_ referências \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span><span class="sxs-lookup"><span data-stu-id="b501c-110">Options of referral chasing as defined in [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span></span> <span data-ttu-id="b501c-111">Quando a caça de referência é definida, a conversão de nome é executada em objetos que não pertencem a esse diretório e são as indicações retornadas da busca de referência.</span><span class="sxs-lookup"><span data-stu-id="b501c-111">When referral chasing is set, the name translation is performed on objects that do not belong to this directory and are the referrals returned from referral chasing.</span></span>

<dt>

<span data-ttu-id="b501c-112">Tipo de acesso: somente gravação</span><span class="sxs-lookup"><span data-stu-id="b501c-112">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="b501c-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="b501c-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="b501c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b501c-114">Remarks</span></span>

<span data-ttu-id="b501c-115">As opções de caça de referência se aplicam somente quando você usa [**IADsNameTranslate:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) e [**IADsNameTranslate:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span><span class="sxs-lookup"><span data-stu-id="b501c-115">The referral chasing options apply only when you use [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) and [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span></span> <span data-ttu-id="b501c-116">O recurso não está disponível com [**IADsNameTranslate:: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) ou [**IADsNameTranslate:: GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span><span class="sxs-lookup"><span data-stu-id="b501c-116">The feature is not available with [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) or [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span></span>

<span data-ttu-id="b501c-117">A interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) tem uma implementação parcial de [**anúncios \_ Chase \_ indicações de referências \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) por meio da propriedade **ChaseReferral** .</span><span class="sxs-lookup"><span data-stu-id="b501c-117">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface has a partial implementation of [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) through the **ChaseReferral** property.</span></span> <span data-ttu-id="b501c-118">Se a propriedade **ChaseReferral** for definida como zero (0), será o mesmo que especificar **anúncios \_ Chase \_ referências \_ nunca** (0).</span><span class="sxs-lookup"><span data-stu-id="b501c-118">If the **ChaseReferral** property is set to zero (0), it is the same as specifying **ADS\_CHASE\_REFERRALS\_NEVER** (0).</span></span> <span data-ttu-id="b501c-119">Se um valor diferente de zero for usado, ele será o mesmo que especificar **anúncios \_ Chase \_ referências \_ sempre** (0x60).</span><span class="sxs-lookup"><span data-stu-id="b501c-119">If a nonzero value is used, it is the same as specifying **ADS\_CHASE\_REFERRALS\_ALWAYS** (0x60).</span></span> <span data-ttu-id="b501c-120">O **IADsNameTranslate** não implementa as opções de **ad \_ Chase \_ \_ subordinadas** (0x20) ou **ADS \_ Chase \_ referências \_ externas** (0x40).</span><span class="sxs-lookup"><span data-stu-id="b501c-120">**IADsNameTranslate** does not implement the **ADS\_CHASE\_REFERRALS\_SUBORDINATE** (0x20) or **ADS\_CHASE\_REFERRALS\_EXTERNAL** (0x40) options.</span></span>

<span data-ttu-id="b501c-121">A configuração padrão para a procura de referência está habilitada (o **ADS \_ Chase as \_ referências \_ sempre**).</span><span class="sxs-lookup"><span data-stu-id="b501c-121">The default setting for referral chasing is enabled (**ADS\_CHASE\_REFERRALS\_ALWAYS**).</span></span> <span data-ttu-id="b501c-122">Sem a busca de referência, você pode fazer com que a conversão de nomes seja executada nesses objetos que residem somente no servidor de diretório conectado.</span><span class="sxs-lookup"><span data-stu-id="b501c-122">Without referral chasing, you can have name translation performed on those objects residing on the connected directory server only.</span></span> <span data-ttu-id="b501c-123">Se você não tiver certeza se o objeto de interesse está no servidor especificado, defina essa propriedade como **ADS \_ Chase \_ referências \_ sempre**.</span><span class="sxs-lookup"><span data-stu-id="b501c-123">If you are uncertain whether the object of interest is on the specified server, you should set this property to be **ADS\_CHASE\_REFERRALS\_ALWAYS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b501c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b501c-124">Requirements</span></span>



| <span data-ttu-id="b501c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b501c-125">Requirement</span></span> | <span data-ttu-id="b501c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b501c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b501c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b501c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b501c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b501c-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b501c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b501c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b501c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b501c-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b501c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b501c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b501c-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="b501c-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b501c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b501c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b501c-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b501c-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b501c-135">IID</span><span class="sxs-lookup"><span data-stu-id="b501c-135">IID</span></span><br/>                      | <span data-ttu-id="b501c-136">IID \_ IADsNameTranslate é definido como B1B272A3-3625-11D1-A3A4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="b501c-136">IID\_IADsNameTranslate is defined as B1B272A3-3625-11D1-A3A4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="b501c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b501c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b501c-138">**Enumeração de referências do ADS \_ Chase \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b501c-138">**ADS\_CHASE\_REFERRALS\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[<span data-ttu-id="b501c-139">**IADsNameTranslate**</span><span class="sxs-lookup"><span data-stu-id="b501c-139">**IADsNameTranslate**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[<span data-ttu-id="b501c-140">**IADsNameTranslate:: Get**</span><span class="sxs-lookup"><span data-stu-id="b501c-140">**IADsNameTranslate::Get**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[<span data-ttu-id="b501c-141">**IADsNameTranslate::GetEx**</span><span class="sxs-lookup"><span data-stu-id="b501c-141">**IADsNameTranslate::GetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[<span data-ttu-id="b501c-142">**IADsNameTranslate:: Set**</span><span class="sxs-lookup"><span data-stu-id="b501c-142">**IADsNameTranslate::Set**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[<span data-ttu-id="b501c-143">**IADsNameTranslate::SetEx**</span><span class="sxs-lookup"><span data-stu-id="b501c-143">**IADsNameTranslate::SetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[<span data-ttu-id="b501c-144">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="b501c-144">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





