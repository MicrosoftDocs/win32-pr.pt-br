---
title: Classe MicrosoftDNS_SIGType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um registro de recurso de assinatura (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- MicrosoftDNS_SIGType de classe de DNS
- MicrosoftDNS_SIGType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644340"
---
# <a name="microsoftdns_sigtype-class"></a><span data-ttu-id="92c4c-105">\_Classe MicrosoftDNS SIGType</span><span class="sxs-lookup"><span data-stu-id="92c4c-105">MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="92c4c-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um registro de recurso de assinatura (SIG).</span><span class="sxs-lookup"><span data-stu-id="92c4c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Signature (SIG) Resource Record.</span></span>

<span data-ttu-id="92c4c-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="92c4c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c4c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92c4c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a><span data-ttu-id="92c4c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="92c4c-109">Members</span></span>

<span data-ttu-id="92c4c-110">A classe **MicrosoftDNS \_ SIGType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="92c4c-110">The **MicrosoftDNS\_SIGType** class has these types of members:</span></span>

-   [<span data-ttu-id="92c4c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="92c4c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="92c4c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92c4c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="92c4c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="92c4c-113">Methods</span></span>

<span data-ttu-id="92c4c-114">A classe **MicrosoftDNS \_ SIGType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="92c4c-114">The **MicrosoftDNS\_SIGType** class has these methods.</span></span>



| <span data-ttu-id="92c4c-115">Método</span><span class="sxs-lookup"><span data-stu-id="92c4c-115">Method</span></span>                             | <span data-ttu-id="92c4c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="92c4c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c4c-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="92c4c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="92c4c-118">Cria uma instância de um RR SIG com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário, a classe (padrão = IN), o valor de vida útil e o sinalizador de mapeamento do WINS, o tempo limite de pesquisa inversa, o tempo limite do cache WINS e o nome de domínio a acrescentar.</span><span class="sxs-lookup"><span data-stu-id="92c4c-118">Instantiates an SIG RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="92c4c-119">Ele retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="92c4c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="92c4c-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="92c4c-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="92c4c-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="92c4c-121">**Modify**</span></span>                         | <span data-ttu-id="92c4c-122">Atualiza o TTL, o sinalizador de mapeamento, o tempo limite de pesquisa, o tempo limite de cache e o domínio de resultado para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="92c4c-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="92c4c-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="92c4c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="92c4c-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="92c4c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="92c4c-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="92c4c-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="92c4c-126">**Windows Server 2003:** Esse método também atualiza TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, Signatárioname e assinatura para os valores especificados como os parâmetros de entrada desse método.</span><span class="sxs-lookup"><span data-stu-id="92c4c-126">**Windows Server 2003:** This method also updates the TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName and Signature to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="92c4c-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92c4c-127">Properties</span></span>

<span data-ttu-id="92c4c-128">A classe **MicrosoftDNS \_ SIGType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="92c4c-128">The **MicrosoftDNS\_SIGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92c4c-129">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="92c4c-129">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c4c-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-132">Algoritmo usado com a chave especificada no registro de recurso.</span><span class="sxs-lookup"><span data-stu-id="92c4c-132">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="92c4c-133">Os valores atribuídos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="92c4c-133">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="92c4c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="92c4c-134">Value</span></span>                                                                                                | <span data-ttu-id="92c4c-135">Significado</span><span class="sxs-lookup"><span data-stu-id="92c4c-135">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="92c4c-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="92c4c-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="92c4c-137">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="92c4c-137">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="92c4c-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="92c4c-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="92c4c-139">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="92c4c-139">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="92c4c-140"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="92c4c-140"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="92c4c-141">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="92c4c-141">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="92c4c-142"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="92c4c-142"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="92c4c-143">Criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="92c4c-143">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="92c4c-144">**KeyTag**</span><span class="sxs-lookup"><span data-stu-id="92c4c-144">**KeyTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-145">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c4c-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-147">Método usado para escolher uma chave que verifica um SIG.</span><span class="sxs-lookup"><span data-stu-id="92c4c-147">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="92c4c-148">Consulte RFC 2535, Apêndice C para o método usado para calcular um KeyTag.</span><span class="sxs-lookup"><span data-stu-id="92c4c-148">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="92c4c-149">**Rótulos**</span><span class="sxs-lookup"><span data-stu-id="92c4c-149">**Labels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c4c-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-152">Contagem não assinada de rótulos no nome do proprietário do RR SIG original.</span><span class="sxs-lookup"><span data-stu-id="92c4c-152">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="92c4c-153">A contagem não inclui o rótulo nulo para a raiz nem qualquer caractere curinga inicial.</span><span class="sxs-lookup"><span data-stu-id="92c4c-153">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="92c4c-154">**OriginalTTL**</span><span class="sxs-lookup"><span data-stu-id="92c4c-154">**OriginalTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-155">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c4c-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-157">TTL do conjunto de RRs assinado pelo SIG.</span><span class="sxs-lookup"><span data-stu-id="92c4c-157">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="92c4c-158">**Signature**</span><span class="sxs-lookup"><span data-stu-id="92c4c-158">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="92c4c-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-161">Assinatura, representada na base 64, formatada conforme definido na RFC 2535, apêndice A.</span><span class="sxs-lookup"><span data-stu-id="92c4c-161">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="92c4c-162">**SignatureExpiration**</span><span class="sxs-lookup"><span data-stu-id="92c4c-162">**SignatureExpiration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-163">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c4c-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-165">Data de expiração da assinatura, expressa em segundos desde o início de 1º de janeiro de 1970, hora de Greenwich (GMT), excluindo segundos bissextos.</span><span class="sxs-lookup"><span data-stu-id="92c4c-165">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="92c4c-166">**SignatureInception**</span><span class="sxs-lookup"><span data-stu-id="92c4c-166">**SignatureInception**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c4c-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-169">Data e hora em que a assinatura se torna válida, expressa em segundos desde o início de 1º de janeiro de 1970, Greenwich Mean Time (GMT), excluindo segundos bissextos.</span><span class="sxs-lookup"><span data-stu-id="92c4c-169">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="92c4c-170">**Signatárioname**</span><span class="sxs-lookup"><span data-stu-id="92c4c-170">**SignerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="92c4c-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-173">Nome de domínio do signatário que gerou o RR SIG.</span><span class="sxs-lookup"><span data-stu-id="92c4c-173">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="92c4c-174">**TypeCovered**</span><span class="sxs-lookup"><span data-stu-id="92c4c-174">**TypeCovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c4c-175">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c4c-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c4c-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92c4c-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c4c-177">Tipo de RR coberto por essa SIG.</span><span class="sxs-lookup"><span data-stu-id="92c4c-177">Type of RR covered by this SIG.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92c4c-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92c4c-178">Requirements</span></span>



| <span data-ttu-id="92c4c-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="92c4c-179">Requirement</span></span> | <span data-ttu-id="92c4c-180">Valor</span><span class="sxs-lookup"><span data-stu-id="92c4c-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92c4c-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92c4c-181">Minimum supported client</span></span><br/> | <span data-ttu-id="92c4c-182">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="92c4c-182">None supported</span></span><br/>                                                              |
| <span data-ttu-id="92c4c-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92c4c-183">Minimum supported server</span></span><br/> | <span data-ttu-id="92c4c-184">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92c4c-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="92c4c-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="92c4c-185">Namespace</span></span><br/>                | <span data-ttu-id="92c4c-186">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="92c4c-186">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="92c4c-187">MOF</span><span class="sxs-lookup"><span data-stu-id="92c4c-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92c4c-188"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92c4c-188"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c4c-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="92c4c-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c4c-190">**Método CreateInstanceFromPropertyData da \_ classe SIGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="92c4c-190">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="92c4c-191">**Método Modify da classe MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="92c4c-191">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="92c4c-192">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="92c4c-192">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





