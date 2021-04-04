---
title: Método CreateInstanceFromPropertyData da classe MicrosoftDNS_SIGType
description: O método CreateInstanceFromPropertyData instancia um registro de recurso de assinatura (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- DNS do método CreateInstanceFromPropertyData
- Método CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType classe DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008989"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="03cc3-106">Método CreateInstanceFromPropertyData da \_ classe SIGType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="03cc3-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="03cc3-107">O método **CreateInstanceFromPropertyData** instancia um registro de recurso de assinatura (SIG).</span><span class="sxs-lookup"><span data-stu-id="03cc3-107">The **CreateInstanceFromPropertyData** method instantiates a Signature (SIG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="03cc3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03cc3-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="03cc3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03cc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03cc3-110">*DnsServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-111">FQDN ou endereço IP do servidor DNS que contém este RR.</span><span class="sxs-lookup"><span data-stu-id="03cc3-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-112">*ContainerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-113">Nome do contêiner para a zona, o cache ou a instância de RootHints que contém esse RR.</span><span class="sxs-lookup"><span data-stu-id="03cc3-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-114">*OwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-115">Nome do proprietário do RR.</span><span class="sxs-lookup"><span data-stu-id="03cc3-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-116">*RecordClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-117">Classe do RR.</span><span class="sxs-lookup"><span data-stu-id="03cc3-117">Class of the RR.</span></span> <span data-ttu-id="03cc3-118">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="03cc3-118">Default value is 1.</span></span> <span data-ttu-id="03cc3-119">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="03cc3-119">The following values are valid.</span></span>



| <span data-ttu-id="03cc3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="03cc3-120">Value</span></span>                                                                                                | <span data-ttu-id="03cc3-121">Significado</span><span class="sxs-lookup"><span data-stu-id="03cc3-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="03cc3-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="03cc3-123">NO (Internet)</span><span class="sxs-lookup"><span data-stu-id="03cc3-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="03cc3-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="03cc3-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="03cc3-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="03cc3-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="03cc3-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="03cc3-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="03cc3-128"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="03cc3-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="03cc3-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="03cc3-130">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-131">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="03cc3-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-132">*TypeCovered* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-132">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-133">Tipo de RR coberto por essa SIG.</span><span class="sxs-lookup"><span data-stu-id="03cc3-133">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-134">*Algoritmo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-134">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-135">Algoritmo usado com a chave especificada no registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="03cc3-135">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="03cc3-136">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="03cc3-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="03cc3-137">Valor</span><span class="sxs-lookup"><span data-stu-id="03cc3-137">Value</span></span>                                                                                                | <span data-ttu-id="03cc3-138">Significado</span><span class="sxs-lookup"><span data-stu-id="03cc3-138">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="03cc3-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-139"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="03cc3-140">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="03cc3-140">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="03cc3-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-141"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="03cc3-142">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="03cc3-142">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="03cc3-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-143"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="03cc3-144">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="03cc3-144">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="03cc3-145"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-145"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="03cc3-146">Criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="03cc3-146">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="03cc3-147">*Rótulos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-147">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-148">Contagem não assinada de rótulos no nome do proprietário do RR SIG original.</span><span class="sxs-lookup"><span data-stu-id="03cc3-148">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="03cc3-149">A contagem não inclui o rótulo nulo para a raiz nem qualquer caractere curinga inicial.</span><span class="sxs-lookup"><span data-stu-id="03cc3-149">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-150">*OriginalTTL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-150">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-151">TTL do conjunto de RRs assinado pelo SIG.</span><span class="sxs-lookup"><span data-stu-id="03cc3-151">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-152">*SignatureExpiration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-152">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-153">Data de expiração da assinatura, expressa em segundos desde o início de 1º de janeiro de 1970, hora de Greenwich (GMT), excluindo segundos bissextos.</span><span class="sxs-lookup"><span data-stu-id="03cc3-153">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-154">*SignatureInception* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-154">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-155">Data e hora em que a assinatura se torna válida, expressa em segundos desde o início de 1º de janeiro de 1970, Greenwich Mean Time (GMT), excluindo segundos bissextos.</span><span class="sxs-lookup"><span data-stu-id="03cc3-155">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-156">*Keytag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-156">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-157">Método usado para escolher uma chave que verifica um SIG.</span><span class="sxs-lookup"><span data-stu-id="03cc3-157">Method used to choose a key that verifies an SIG.</span></span> <span data-ttu-id="03cc3-158">Consulte RFC 2535, Apêndice C para o método usado para calcular um KeyTag.</span><span class="sxs-lookup"><span data-stu-id="03cc3-158">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-159">*Signatárioname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-159">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-160">Nome de domínio do signatário que gerou o RR SIG.</span><span class="sxs-lookup"><span data-stu-id="03cc3-160">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-161">*Assinatura* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-161">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-162">Assinatura, representada na base 64, formatada conforme definido na RFC 2535, apêndice A.</span><span class="sxs-lookup"><span data-stu-id="03cc3-162">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="03cc3-163">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-163">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="03cc3-164">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="03cc3-164">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03cc3-165">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03cc3-165">Return value</span></span>

<span data-ttu-id="03cc3-166">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="03cc3-166">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03cc3-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03cc3-167">Requirements</span></span>



| <span data-ttu-id="03cc3-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="03cc3-168">Requirement</span></span> | <span data-ttu-id="03cc3-169">Valor</span><span class="sxs-lookup"><span data-stu-id="03cc3-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03cc3-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03cc3-170">Minimum supported client</span></span><br/> | <span data-ttu-id="03cc3-171">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="03cc3-171">None supported</span></span><br/>                                                              |
| <span data-ttu-id="03cc3-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03cc3-172">Minimum supported server</span></span><br/> | <span data-ttu-id="03cc3-173">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03cc3-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="03cc3-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="03cc3-174">Namespace</span></span><br/>                | <span data-ttu-id="03cc3-175">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="03cc3-175">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="03cc3-176">MOF</span><span class="sxs-lookup"><span data-stu-id="03cc3-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03cc3-177"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03cc3-177"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03cc3-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="03cc3-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03cc3-179">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="03cc3-179">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="03cc3-180">**Método Modify da classe MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="03cc3-180">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="03cc3-181">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="03cc3-181">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





