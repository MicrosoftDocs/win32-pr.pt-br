---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_ATMAType
description: O método CreateInstanceFromPropertyData instancia um endereço ATM para um registro de recurso de nome (ATMA).
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755640"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="65ba4-106">Método CreateInstanceFromPropertyData da \_ classe ATMAType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="65ba4-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="65ba4-107">O método **CreateInstanceFromPropertyData** instancia um endereço ATM para um registro de recurso de nome (ATMA).</span><span class="sxs-lookup"><span data-stu-id="65ba4-107">The **CreateInstanceFromPropertyData** method instantiates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ba4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65ba4-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="65ba4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65ba4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ba4-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ba4-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="65ba4-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="65ba4-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ba4-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="65ba4-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="65ba4-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ba4-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="65ba4-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="65ba4-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65ba4-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="65ba4-117">Class of the RR.</span></span> <span data-ttu-id="65ba4-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="65ba4-118">Default value is 1.</span></span> <span data-ttu-id="65ba4-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="65ba4-119">The following values are valid.</span></span>



| <span data-ttu-id="65ba4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="65ba4-120">Value</span></span>                                                                                                | <span data-ttu-id="65ba4-121">Significado</span><span class="sxs-lookup"><span data-stu-id="65ba4-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="65ba4-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="65ba4-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="65ba4-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="65ba4-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="65ba4-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="65ba4-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="65ba4-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="65ba4-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="65ba4-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="65ba4-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="65ba4-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="65ba4-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="65ba4-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="65ba4-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="65ba4-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="65ba4-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="65ba4-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="65ba4-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="65ba4-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="65ba4-132">*Formato* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ba4-133">Formato de endereço ATM.</span><span class="sxs-lookup"><span data-stu-id="65ba4-133">ATM address format.</span></span> <span data-ttu-id="65ba4-134">Dois valores possíveis para o formato são: 0 indicando o formato de endereço do sistema final do ATM (AESA) e 1 indicando o formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="65ba4-134">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="65ba4-135">*ATMAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-135">*ATMAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65ba4-136">Cadeia de caracteres de comprimento variável de octetos que contém o endereço ATM do nó/proprietário ao qual esse RR pertence.</span><span class="sxs-lookup"><span data-stu-id="65ba4-136">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="65ba4-137">Os primeiros quatro bytes da matriz são usados para armazenar o tamanho da cadeia de caracteres do octeto.</span><span class="sxs-lookup"><span data-stu-id="65ba4-137">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="65ba4-138">O byte mais significativo é armazenado em byte 0.</span><span class="sxs-lookup"><span data-stu-id="65ba4-138">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="65ba4-139">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="65ba4-140">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="65ba4-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ba4-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65ba4-141">Return value</span></span>

<span data-ttu-id="65ba4-142">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="65ba4-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ba4-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65ba4-143">Requirements</span></span>



| <span data-ttu-id="65ba4-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="65ba4-144">Requirement</span></span> | <span data-ttu-id="65ba4-145">Valor</span><span class="sxs-lookup"><span data-stu-id="65ba4-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65ba4-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65ba4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="65ba4-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="65ba4-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="65ba4-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65ba4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="65ba4-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="65ba4-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="65ba4-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="65ba4-150">Namespace</span></span><br/>                | <span data-ttu-id="65ba4-151">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="65ba4-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="65ba4-152">MOF</span><span class="sxs-lookup"><span data-stu-id="65ba4-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65ba4-153"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65ba4-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ba4-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="65ba4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ba4-155">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="65ba4-155">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="65ba4-156">**Método Modify da classe MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="65ba4-156">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="65ba4-157">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="65ba4-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





