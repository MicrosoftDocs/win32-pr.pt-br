---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_AFSDBType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso do servidor de banco de dados do sistema de arquivos Andrew (AFSDB).
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918459"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="166cc-106">Método CreateInstanceFromPropertyData da \_ classe AFSDBType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="166cc-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="166cc-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso do servidor de banco de dados do sistema de arquivos Andrew (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="166cc-107">The **CreateInstanceFromPropertyData** method instantiates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="166cc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="166cc-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="166cc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="166cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="166cc-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="166cc-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166cc-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="166cc-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="166cc-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="166cc-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166cc-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="166cc-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="166cc-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="166cc-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166cc-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="166cc-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="166cc-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="166cc-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="166cc-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="166cc-117">Class of the RR.</span></span> <span data-ttu-id="166cc-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="166cc-118">Default value is 1.</span></span> <span data-ttu-id="166cc-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="166cc-119">The following values are valid.</span></span>



| <span data-ttu-id="166cc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="166cc-120">Value</span></span>                                                                                                | <span data-ttu-id="166cc-121">Significado</span><span class="sxs-lookup"><span data-stu-id="166cc-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="166cc-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="166cc-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="166cc-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="166cc-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="166cc-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="166cc-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="166cc-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="166cc-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="166cc-126"><dt>**Beta**</dt></span><span class="sxs-lookup"><span data-stu-id="166cc-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="166cc-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="166cc-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="166cc-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="166cc-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="166cc-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="166cc-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="166cc-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="166cc-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="166cc-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="166cc-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="166cc-132">*Subtipo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="166cc-132">*Subtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166cc-133">Subtipo do servidor host AFS.</span><span class="sxs-lookup"><span data-stu-id="166cc-133">Subtype of the host AFS server.</span></span> <span data-ttu-id="166cc-134">Para o subtipo 1 (valor = 1), o host tem um servidor de local de volume AFS versão 3,0 para a célula AFS nomeada.</span><span class="sxs-lookup"><span data-stu-id="166cc-134">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="166cc-135">No caso do subtipo 2 (valor = 2), o host tem um servidor de nomes autenticado que contém o nó do diretório raiz da célula para a célula de DCE/NCA nomeada.</span><span class="sxs-lookup"><span data-stu-id="166cc-135">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="166cc-136">*Nome do Server* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="166cc-136">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="166cc-137">FQDN que especifica um host que tem um servidor para a célula AFS especificada no nome do proprietário.</span><span class="sxs-lookup"><span data-stu-id="166cc-137">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="166cc-138">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="166cc-138">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="166cc-139">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="166cc-139">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="166cc-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="166cc-140">Return value</span></span>

<span data-ttu-id="166cc-141">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="166cc-141">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="166cc-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="166cc-142">Requirements</span></span>



| <span data-ttu-id="166cc-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="166cc-143">Requirement</span></span> | <span data-ttu-id="166cc-144">Valor</span><span class="sxs-lookup"><span data-stu-id="166cc-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="166cc-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="166cc-145">Minimum supported client</span></span><br/> | <span data-ttu-id="166cc-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="166cc-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="166cc-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="166cc-147">Minimum supported server</span></span><br/> | <span data-ttu-id="166cc-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="166cc-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="166cc-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="166cc-149">Namespace</span></span><br/>                | <span data-ttu-id="166cc-150">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="166cc-150">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="166cc-151">MOF</span><span class="sxs-lookup"><span data-stu-id="166cc-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="166cc-152"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="166cc-152"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="166cc-153">Consulte também</span><span class="sxs-lookup"><span data-stu-id="166cc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="166cc-154">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="166cc-154">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="166cc-155">**Método Modify da classe MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="166cc-155">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="166cc-156">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="166cc-156">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





