---
title: Método CreateInstanceFromTextRepresentation da classe MicrosoftDNS_ResourceRecord
description: O método CreateInstanceFromTextRepresentation instancia um objeto MicrosoftDNS \_ ResourceRecord.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- DNS do método CreateInstanceFromTextRepresentation
- Método CreateInstanceFromTextRepresentation DNS, classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord classe DNS, método CreateInstanceFromTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009477"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="50b45-106">Método CreateInstanceFromTextRepresentation da \_ classe ResourceRecord MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="50b45-106">CreateInstanceFromTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="50b45-107">O método **CreateInstanceFromTextRepresentation** instancia um objeto [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .</span><span class="sxs-lookup"><span data-stu-id="50b45-107">The **CreateInstanceFromTextRepresentation** method instantiates a [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b45-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50b45-108">Syntax</span></span>


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a><span data-ttu-id="50b45-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50b45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b45-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50b45-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b45-111">Nome do servidor DNS no qual o RR deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="50b45-111">Name of the DNS Server on which the RR should be created.</span></span>

</dd> <dt>

<span data-ttu-id="50b45-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50b45-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b45-113">Nome do contêiner no qual o novo RR deve ser colocado.</span><span class="sxs-lookup"><span data-stu-id="50b45-113">Name of the container into which the new RR should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="50b45-114">*Textrepresentation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50b45-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b45-115">Representação de texto da instância de RR a ser criada.</span><span class="sxs-lookup"><span data-stu-id="50b45-115">Text representation of the RR instance to be created.</span></span>

</dd> <dt>

<span data-ttu-id="50b45-116">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="50b45-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="50b45-117">Referência ao RR instanciado.</span><span class="sxs-lookup"><span data-stu-id="50b45-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b45-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50b45-118">Return value</span></span>

<span data-ttu-id="50b45-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="50b45-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b45-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50b45-120">Requirements</span></span>



| <span data-ttu-id="50b45-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="50b45-121">Requirement</span></span> | <span data-ttu-id="50b45-122">Valor</span><span class="sxs-lookup"><span data-stu-id="50b45-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50b45-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50b45-123">Minimum supported client</span></span><br/> | <span data-ttu-id="50b45-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="50b45-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="50b45-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50b45-125">Minimum supported server</span></span><br/> | <span data-ttu-id="50b45-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="50b45-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="50b45-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="50b45-127">Namespace</span></span><br/>                | <span data-ttu-id="50b45-128">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="50b45-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="50b45-129">MOF</span><span class="sxs-lookup"><span data-stu-id="50b45-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50b45-130"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50b45-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b45-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="50b45-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b45-132">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="50b45-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="50b45-133">**Método GetObjectByTextRepresentation da \_ classe ResourceRecord MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="50b45-133">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





