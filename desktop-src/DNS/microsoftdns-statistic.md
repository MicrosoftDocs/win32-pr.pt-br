---
title: Classe MicrosoftDNS_Statistic
description: A \_ classe de estatística MicrosoftDNS representa uma única estatística de servidor DNS.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- MicrosoftDNS_Statistic de classe de DNS
- MicrosoftDNS_Statistic de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009644"
---
# <a name="microsoftdns_statistic-class"></a><span data-ttu-id="a5e6a-105">\_Classe de estatística MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="a5e6a-105">MicrosoftDNS\_Statistic class</span></span>

<span data-ttu-id="a5e6a-106">A classe de **\_ estatística MicrosoftDNS** representa uma única estatística de servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-106">The **MicrosoftDNS\_Statistic** class represents a single DNS Server statistic.</span></span>

<span data-ttu-id="a5e6a-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e6a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5e6a-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a><span data-ttu-id="a5e6a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a5e6a-109">Members</span></span>

<span data-ttu-id="a5e6a-110">A classe de **\_ estatística MicrosoftDNS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a5e6a-110">The **MicrosoftDNS\_Statistic** class has these types of members:</span></span>

-   [<span data-ttu-id="a5e6a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a5e6a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5e6a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a5e6a-112">Properties</span></span>

<span data-ttu-id="a5e6a-113">A classe de **\_ estatística MicrosoftDNS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-113">The **MicrosoftDNS\_Statistic** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5e6a-114">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-114">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-115">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5e6a-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5e6a-117">Representação numérica de **CollectionName**.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-117">Numeric representation of **CollectionName**.</span></span>

</dd> <dt>

<span data-ttu-id="a5e6a-118">**CollectionName**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-118">**CollectionName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5e6a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5e6a-121">Nome da coleção à qual a estatística pertence.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-121">Name of the collection to which the statistic belongs.</span></span>

</dd> <dt>

<span data-ttu-id="a5e6a-122">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-122">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5e6a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5e6a-125">Indica o FQDN ou o endereço IP do servidor DNS que contém a estatística.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-125">Indicates the FQDN or IP address of the DNS Server that contains the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="a5e6a-126">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-126">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5e6a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5e6a-129">Nome da estatística.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-129">Name of the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="a5e6a-130">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-130">**StringValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5e6a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5e6a-133">Valor da cadeia de caracteres da estatística, usado somente quando o valor da estatística não é representado como um DWORD.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-133">String value of the statistic, used only when the statistic value is not represented as a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="a5e6a-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-134">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5e6a-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5e6a-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5e6a-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5e6a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5e6a-137">Valor numérico da estatística, representado como um DWORD.</span><span class="sxs-lookup"><span data-stu-id="a5e6a-137">Numeric value of the statistic, represented as a DWORD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5e6a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5e6a-138">Requirements</span></span>



| <span data-ttu-id="a5e6a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5e6a-139">Requirement</span></span> | <span data-ttu-id="a5e6a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="a5e6a-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e6a-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5e6a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e6a-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a5e6a-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a5e6a-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5e6a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e6a-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a5e6a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a5e6a-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5e6a-145">Namespace</span></span><br/>                | <span data-ttu-id="a5e6a-146">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="a5e6a-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a5e6a-147">MOF</span><span class="sxs-lookup"><span data-stu-id="a5e6a-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5e6a-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5e6a-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5e6a-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5e6a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e6a-150">\_Estatísticacollection de MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="a5e6a-150">MicrosoftDNS\_StatisticCollection</span></span>](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





