---
title: Método Modify da classe MicrosoftDNS_X25Type
description: O método Modify atualiza um registro de recurso X. 25 (X25).
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_X25Type classe
- MicrosoftDNS_X25Type classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10db2fa770d3da8487a712e631c41fdd4256bf7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085799"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="099d6-106">Método Modify da classe MicrosoftDNS \_ X25Type</span><span class="sxs-lookup"><span data-stu-id="099d6-106">Modify method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="099d6-107">O método **Modify** atualiza um registro de recurso X. 25 (X25).</span><span class="sxs-lookup"><span data-stu-id="099d6-107">The **Modify** method updates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="099d6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="099d6-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="099d6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="099d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099d6-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="099d6-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="099d6-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="099d6-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="099d6-112">*PSDNAddress* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="099d6-112">*PSDNAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="099d6-113">Endereço PSDN do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="099d6-113">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="099d6-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="099d6-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="099d6-115">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="099d6-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099d6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="099d6-116">Return value</span></span>

<span data-ttu-id="099d6-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="099d6-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="099d6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="099d6-118">Remarks</span></span>

<span data-ttu-id="099d6-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="099d6-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="099d6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="099d6-120">Requirements</span></span>



| <span data-ttu-id="099d6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="099d6-121">Requirement</span></span> | <span data-ttu-id="099d6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="099d6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="099d6-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="099d6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="099d6-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="099d6-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="099d6-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="099d6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="099d6-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="099d6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="099d6-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="099d6-127">Namespace</span></span><br/>                | <span data-ttu-id="099d6-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="099d6-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="099d6-129">MOF</span><span class="sxs-lookup"><span data-stu-id="099d6-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="099d6-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="099d6-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099d6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="099d6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099d6-132">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="099d6-132">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="099d6-133">**Método CreateInstanceFromPropertyData da \_ classe X25Type MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="099d6-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="099d6-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="099d6-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





