---
title: Método Modify da classe MicrosoftDNS_PTRType
description: O método Modify atualiza um registro de recurso de ponteiro (PTR).
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_PTRType classe
- MicrosoftDNS_PTRType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918604"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="d6e71-106">Método Modify da classe MicrosoftDNS \_ PTRType</span><span class="sxs-lookup"><span data-stu-id="d6e71-106">Modify method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="d6e71-107">O método **Modify** atualiza um registro de recurso de ponteiro (PTR).</span><span class="sxs-lookup"><span data-stu-id="d6e71-107">The **Modify** method updates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e71-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6e71-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d6e71-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6e71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e71-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d6e71-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e71-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="d6e71-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d6e71-112">*PTRDomainName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d6e71-112">*PTRDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e71-113">Endereço do nome de domínio do registro PTR.</span><span class="sxs-lookup"><span data-stu-id="d6e71-113">Domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="d6e71-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="d6e71-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d6e71-115">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="d6e71-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e71-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6e71-116">Return value</span></span>

<span data-ttu-id="d6e71-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d6e71-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6e71-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6e71-118">Remarks</span></span>

<span data-ttu-id="d6e71-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="d6e71-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e71-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6e71-120">Requirements</span></span>



| <span data-ttu-id="d6e71-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6e71-121">Requirement</span></span> | <span data-ttu-id="d6e71-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d6e71-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e71-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6e71-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e71-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d6e71-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d6e71-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6e71-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e71-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d6e71-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d6e71-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6e71-127">Namespace</span></span><br/>                | <span data-ttu-id="d6e71-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="d6e71-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d6e71-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d6e71-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6e71-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6e71-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6e71-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6e71-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e71-132">**MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="d6e71-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="d6e71-133">**Método CreateInstanceFromPropertyData da \_ classe PTRType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="d6e71-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d6e71-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d6e71-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





