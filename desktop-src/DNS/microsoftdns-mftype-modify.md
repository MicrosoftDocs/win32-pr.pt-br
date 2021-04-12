---
title: Método Modify da classe MicrosoftDNS_MFType
description: O método Modify atualiza um registro de recurso do agente de encaminhamento de mensagens para o domínio (MF).
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_MFType classe
- MicrosoftDNS_MFType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0a363290580c7cecf47dbe00c6dd7895d23dbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455521"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="3798b-106">Método Modify da classe MicrosoftDNS \_ MFType</span><span class="sxs-lookup"><span data-stu-id="3798b-106">Modify method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="3798b-107">O método **Modify** atualiza um registro de recurso do agente de encaminhamento de mensagens para o domínio (MF).</span><span class="sxs-lookup"><span data-stu-id="3798b-107">The **Modify** method updates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3798b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3798b-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3798b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3798b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3798b-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3798b-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3798b-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="3798b-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3798b-112">*MFHost* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3798b-112">*MFHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3798b-113">Nome do host que fornece o agente de encaminhamento de email.</span><span class="sxs-lookup"><span data-stu-id="3798b-113">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="3798b-114">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="3798b-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3798b-115">Referência ao objeto modificado.</span><span class="sxs-lookup"><span data-stu-id="3798b-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3798b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3798b-116">Return value</span></span>

<span data-ttu-id="3798b-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3798b-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3798b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3798b-118">Remarks</span></span>

<span data-ttu-id="3798b-119">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="3798b-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3798b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3798b-120">Requirements</span></span>



| <span data-ttu-id="3798b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3798b-121">Requirement</span></span> | <span data-ttu-id="3798b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3798b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3798b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3798b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3798b-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3798b-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3798b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3798b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3798b-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3798b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3798b-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3798b-127">Namespace</span></span><br/>                | <span data-ttu-id="3798b-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="3798b-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3798b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3798b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3798b-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3798b-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3798b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3798b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3798b-132">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="3798b-132">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="3798b-133">**Método CreateInstanceFromPropertyData da \_ classe MFType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="3798b-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3798b-134">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3798b-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





