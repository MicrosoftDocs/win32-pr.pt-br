---
title: Método Modify da classe MicrosoftDNS_RTType
description: O método Modify atualiza um registro de recurso de rota a (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_RTType classe
- MicrosoftDNS_RTType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499428"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="cfe50-106">Método Modify da classe MicrosoftDNS \_ RTType</span><span class="sxs-lookup"><span data-stu-id="cfe50-106">Modify method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="cfe50-107">O método **Modify** atualiza um registro de recurso de rota a (RT).</span><span class="sxs-lookup"><span data-stu-id="cfe50-107">The **Modify** method updates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe50-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfe50-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="cfe50-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfe50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe50-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cfe50-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe50-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="cfe50-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="cfe50-112">*Preferência* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cfe50-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe50-113">Preferência dada a esse RR entre outros no mesmo proprietário.</span><span class="sxs-lookup"><span data-stu-id="cfe50-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="cfe50-114">Os valores mais baixos são preferenciais.</span><span class="sxs-lookup"><span data-stu-id="cfe50-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="cfe50-115">*IntermediateHost* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cfe50-115">*IntermediateHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe50-116">FQDN que especifica um host para servir como intermediário para atingir o host especificado pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="cfe50-116">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="cfe50-117">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="cfe50-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe50-118">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="cfe50-118">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe50-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfe50-119">Return value</span></span>

<span data-ttu-id="cfe50-120">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cfe50-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe50-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfe50-121">Remarks</span></span>

<span data-ttu-id="cfe50-122">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="cfe50-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe50-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfe50-123">Requirements</span></span>



| <span data-ttu-id="cfe50-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe50-124">Requirement</span></span> | <span data-ttu-id="cfe50-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cfe50-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe50-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfe50-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe50-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cfe50-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cfe50-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfe50-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe50-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cfe50-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cfe50-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfe50-130">Namespace</span></span><br/>                | <span data-ttu-id="cfe50-131">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="cfe50-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cfe50-132">MOF</span><span class="sxs-lookup"><span data-stu-id="cfe50-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfe50-133"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfe50-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe50-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfe50-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe50-135">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="cfe50-135">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="cfe50-136">**Método CreateInstanceFromPropertyData da \_ classe RTType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="cfe50-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="cfe50-137">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="cfe50-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





