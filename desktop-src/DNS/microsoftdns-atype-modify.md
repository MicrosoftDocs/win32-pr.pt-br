---
title: Método Modify da classe MicrosoftDNS_AType
description: O método Modify atualiza o TTL e o endereço IP de um registro de recurso de endereço de host (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_AType classe
- MicrosoftDNS_AType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009379"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="58f37-106">Método Modify da classe MicrosoftDNS \_ AType</span><span class="sxs-lookup"><span data-stu-id="58f37-106">Modify method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="58f37-107">O método **Modify** atualiza o TTL e o endereço IP de um registro de recurso de endereço de host (a).</span><span class="sxs-lookup"><span data-stu-id="58f37-107">The **Modify** method updates the TTL and IP address of a host Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f37-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58f37-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="58f37-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58f37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f37-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="58f37-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58f37-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="58f37-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="58f37-112">*IPAddress* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="58f37-112">*IPAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58f37-113">Cadeia de caracteres que representa o endereço IP do host.</span><span class="sxs-lookup"><span data-stu-id="58f37-113">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="58f37-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="58f37-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="58f37-115">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="58f37-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f37-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58f37-116">Return value</span></span>

<span data-ttu-id="58f37-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="58f37-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58f37-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="58f37-118">Remarks</span></span>

<span data-ttu-id="58f37-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="58f37-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f37-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58f37-120">Requirements</span></span>



| <span data-ttu-id="58f37-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="58f37-121">Requirement</span></span> | <span data-ttu-id="58f37-122">Valor</span><span class="sxs-lookup"><span data-stu-id="58f37-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58f37-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58f37-123">Minimum supported client</span></span><br/> | <span data-ttu-id="58f37-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="58f37-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="58f37-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58f37-125">Minimum supported server</span></span><br/> | <span data-ttu-id="58f37-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58f37-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="58f37-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="58f37-127">Namespace</span></span><br/>                | <span data-ttu-id="58f37-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="58f37-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="58f37-129">MOF</span><span class="sxs-lookup"><span data-stu-id="58f37-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58f37-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58f37-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f37-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="58f37-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f37-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="58f37-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="58f37-133">**Método CreateInstanceFromPropertyData da \_ classe AType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="58f37-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





