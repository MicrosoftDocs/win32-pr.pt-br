---
title: Método Modify da classe MicrosoftDNS_MBType
description: O método Modify atualiza um registro de recurso de caixa de correio (MB).
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MBType classe
- MicrosoftDNS_MBType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d6f0fcb0faf5c1e8da152798863c8cecc8641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644772"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="407f5-106">Método Modify da classe MicrosoftDNS \_ MBType</span><span class="sxs-lookup"><span data-stu-id="407f5-106">Modify method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="407f5-107">O método **Modify** atualiza um registro de recurso de caixa de correio (MB).</span><span class="sxs-lookup"><span data-stu-id="407f5-107">The **Modify** method updates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="407f5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="407f5-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="407f5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="407f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="407f5-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="407f5-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="407f5-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="407f5-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="407f5-112">*MBHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="407f5-112">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="407f5-113">Cadeia de caracteres que representa o nome do host da caixa de correio para o registro de MB.</span><span class="sxs-lookup"><span data-stu-id="407f5-113">String representing the mailbox host name for the MB record.</span></span>

</dd> <dt>

<span data-ttu-id="407f5-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="407f5-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="407f5-115">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="407f5-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="407f5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="407f5-116">Return value</span></span>

<span data-ttu-id="407f5-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="407f5-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="407f5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="407f5-118">Remarks</span></span>

<span data-ttu-id="407f5-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="407f5-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="407f5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="407f5-120">Requirements</span></span>



| <span data-ttu-id="407f5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="407f5-121">Requirement</span></span> | <span data-ttu-id="407f5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="407f5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="407f5-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="407f5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="407f5-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="407f5-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="407f5-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="407f5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="407f5-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="407f5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="407f5-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="407f5-127">Namespace</span></span><br/>                | <span data-ttu-id="407f5-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="407f5-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="407f5-129">MOF</span><span class="sxs-lookup"><span data-stu-id="407f5-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="407f5-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="407f5-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="407f5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="407f5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407f5-132">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="407f5-132">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="407f5-133">**Método CreateInstanceFromPropertyData da \_ classe MBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="407f5-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="407f5-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="407f5-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





