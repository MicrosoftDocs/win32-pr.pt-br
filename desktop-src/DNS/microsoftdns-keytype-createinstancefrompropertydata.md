---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_KEYType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de chave.
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16dc8f3f591ba3aaf5ac9883cdd3a15c85146d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009735"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="62c33-106">Método CreateInstanceFromPropertyData da \_ classe KeyType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="62c33-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="62c33-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de chave.</span><span class="sxs-lookup"><span data-stu-id="62c33-107">The **CreateInstanceFromPropertyData** method instantiates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c33-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62c33-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="62c33-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62c33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c33-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62c33-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="62c33-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="62c33-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62c33-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="62c33-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="62c33-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62c33-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="62c33-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="62c33-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="62c33-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="62c33-117">Class of the RR.</span></span> <span data-ttu-id="62c33-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="62c33-118">Default value is 1.</span></span> <span data-ttu-id="62c33-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="62c33-119">The following values are valid.</span></span>



| <span data-ttu-id="62c33-120">Valor</span><span class="sxs-lookup"><span data-stu-id="62c33-120">Value</span></span>                                                                                                | <span data-ttu-id="62c33-121">Significado</span><span class="sxs-lookup"><span data-stu-id="62c33-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="62c33-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="62c33-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="62c33-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="62c33-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="62c33-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="62c33-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="62c33-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="62c33-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="62c33-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="62c33-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="62c33-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="62c33-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="62c33-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="62c33-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="62c33-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="62c33-132">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="62c33-132">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-133">Sinalizadores usados para especificar o mapeamento, conforme descrito em IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="62c33-133">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="62c33-134">*Protocolo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="62c33-134">*Protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-135">Protocolo para o qual a chave especificada no registro de recurso pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="62c33-135">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="62c33-136">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="62c33-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="62c33-137">Valor</span><span class="sxs-lookup"><span data-stu-id="62c33-137">Value</span></span>                                                                                                    | <span data-ttu-id="62c33-138">Significado</span><span class="sxs-lookup"><span data-stu-id="62c33-138">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="62c33-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-139"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="62c33-140">TLS</span><span class="sxs-lookup"><span data-stu-id="62c33-140">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="62c33-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-141"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="62c33-142">Email</span><span class="sxs-lookup"><span data-stu-id="62c33-142">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="62c33-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-143"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="62c33-144">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="62c33-144">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="62c33-145"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-145"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="62c33-146">IPsec</span><span class="sxs-lookup"><span data-stu-id="62c33-146">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="62c33-147"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-147"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="62c33-148">Todos os protocolos</span><span class="sxs-lookup"><span data-stu-id="62c33-148">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62c33-149">*Algoritmo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="62c33-149">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-150">Algoritmo usado com a chave especificada no registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="62c33-150">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="62c33-151">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="62c33-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="62c33-152">Valor</span><span class="sxs-lookup"><span data-stu-id="62c33-152">Value</span></span>                                                                                                | <span data-ttu-id="62c33-153">Significado</span><span class="sxs-lookup"><span data-stu-id="62c33-153">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="62c33-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-154"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="62c33-155">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="62c33-155">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="62c33-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-156"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="62c33-157">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="62c33-157">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="62c33-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-158"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="62c33-159">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="62c33-159">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="62c33-160"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-160"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="62c33-161">Criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="62c33-161">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62c33-162">*PublicKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62c33-162">*PublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-163">Chave pública, representada na base 64, conforme descrito no apêndice A de RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="62c33-163">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="62c33-164">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="62c33-164">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="62c33-165">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="62c33-165">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c33-166">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62c33-166">Return value</span></span>

<span data-ttu-id="62c33-167">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="62c33-167">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c33-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62c33-168">Requirements</span></span>



| <span data-ttu-id="62c33-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c33-169">Requirement</span></span> | <span data-ttu-id="62c33-170">Valor</span><span class="sxs-lookup"><span data-stu-id="62c33-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c33-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62c33-171">Minimum supported client</span></span><br/> | <span data-ttu-id="62c33-172">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="62c33-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="62c33-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62c33-173">Minimum supported server</span></span><br/> | <span data-ttu-id="62c33-174">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="62c33-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="62c33-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="62c33-175">Namespace</span></span><br/>                | <span data-ttu-id="62c33-176">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="62c33-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="62c33-177">MOF</span><span class="sxs-lookup"><span data-stu-id="62c33-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62c33-178"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62c33-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c33-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="62c33-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c33-180">**KeyType MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="62c33-180">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="62c33-181">**Método Modify da \_ classe KeyType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="62c33-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="62c33-182">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="62c33-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





