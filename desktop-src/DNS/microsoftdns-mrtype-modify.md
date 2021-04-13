---
title: Método Modify da classe MicrosoftDNS_MRType
description: O método Modify atualiza um registro de recurso MR (renomeação da caixa de correio).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MRType classe
- MicrosoftDNS_MRType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455105"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="3d8ed-106">Método Modify da classe MicrosoftDNS \_ MRType</span><span class="sxs-lookup"><span data-stu-id="3d8ed-106">Modify method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="3d8ed-107">O método **Modify** atualiza um registro de recurso Mr (renomeação da caixa de correio).</span><span class="sxs-lookup"><span data-stu-id="3d8ed-107">The **Modify** method updates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8ed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d8ed-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3d8ed-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d8ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d8ed-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3d8ed-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8ed-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3d8ed-112">*MRMailbox* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3d8ed-112">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8ed-113">FQDN que especifica uma caixa de correio que é a renomeação correta da caixa de correio especificada no nome do proprietário do registro.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-113">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="3d8ed-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="3d8ed-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8ed-115">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d8ed-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d8ed-116">Return value</span></span>

<span data-ttu-id="3d8ed-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8ed-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d8ed-118">Remarks</span></span>

<span data-ttu-id="3d8ed-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d8ed-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d8ed-120">Requirements</span></span>



| <span data-ttu-id="3d8ed-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d8ed-121">Requirement</span></span> | <span data-ttu-id="3d8ed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3d8ed-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8ed-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d8ed-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3d8ed-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3d8ed-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3d8ed-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d8ed-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3d8ed-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d8ed-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3d8ed-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d8ed-127">Namespace</span></span><br/>                | <span data-ttu-id="3d8ed-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="3d8ed-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3d8ed-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3d8ed-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d8ed-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d8ed-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d8ed-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d8ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8ed-132">**MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="3d8ed-132">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="3d8ed-133">**Método CreateInstanceFromPropertyData da \_ classe MRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3d8ed-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3d8ed-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3d8ed-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





