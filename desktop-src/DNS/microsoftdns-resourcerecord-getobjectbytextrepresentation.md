---
title: Método GetObjectByTextRepresentation da classe MicrosoftDNS_ResourceRecord
description: O método GetObjectByTextRepresentation recupera uma instância existente da classe MicrosoftDNS \_ ResourceRecord.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- DNS do método GetObjectByTextRepresentation
- Método GetObjectByTextRepresentation DNS, classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord classe DNS, método GetObjectByTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455333"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="fed71-106">Método GetObjectByTextRepresentation da \_ classe ResourceRecord MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="fed71-106">GetObjectByTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="fed71-107">O método **GetObjectByTextRepresentation** recupera uma instância existente da classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="fed71-107">The **GetObjectByTextRepresentation** method retrieves an existing instance of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed71-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fed71-108">Syntax</span></span>


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a><span data-ttu-id="fed71-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fed71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed71-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fed71-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fed71-111">Nome do servidor DNS do qual o RR deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="fed71-111">Name of the DNS Server from which the RR should be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="fed71-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fed71-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fed71-113">Nome do contêiner do qual o RR deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="fed71-113">Name of the container from which the RR should be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="fed71-114">*Textrepresentation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fed71-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fed71-115">Representação de texto do RR a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="fed71-115">Text representation of the RR to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="fed71-116">*RR* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fed71-116">*RR* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fed71-117">Referência ao RR instanciado.</span><span class="sxs-lookup"><span data-stu-id="fed71-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed71-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fed71-118">Return value</span></span>

<span data-ttu-id="fed71-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fed71-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed71-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fed71-120">Requirements</span></span>



| <span data-ttu-id="fed71-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed71-121">Requirement</span></span> | <span data-ttu-id="fed71-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fed71-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fed71-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fed71-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fed71-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fed71-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fed71-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fed71-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fed71-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fed71-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fed71-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fed71-127">Namespace</span></span><br/>                | <span data-ttu-id="fed71-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="fed71-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fed71-129">MOF</span><span class="sxs-lookup"><span data-stu-id="fed71-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fed71-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fed71-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed71-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fed71-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed71-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="fed71-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="fed71-133">**Método CreateInstanceFromTextRepresentation da \_ classe ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="fed71-133">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





