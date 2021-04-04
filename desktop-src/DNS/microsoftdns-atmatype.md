---
title: Classe MicrosoftDNS_ATMAType
description: A subclasse de MicrosoftDNS \_ ResourceRecord que representa um endereço de ATM para um registro de nome (ATMA).
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- MicrosoftDNS_ATMAType de classe de DNS
- MicrosoftDNS_ATMAType de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918455"
---
# <a name="microsoftdns_atmatype-class"></a><span data-ttu-id="c1911-105">\_Classe MicrosoftDNS ATMAType</span><span class="sxs-lookup"><span data-stu-id="c1911-105">MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="c1911-106">A subclasse de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa um endereço de ATM para um registro de nome (ATMA).</span><span class="sxs-lookup"><span data-stu-id="c1911-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents an ATM Address to Name (ATMA) record.</span></span>

<span data-ttu-id="c1911-107">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c1911-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1911-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1911-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a><span data-ttu-id="c1911-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c1911-109">Members</span></span>

<span data-ttu-id="c1911-110">A classe **MicrosoftDNS \_ ATMAType** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1911-110">The **MicrosoftDNS\_ATMAType** class has these types of members:</span></span>

-   [<span data-ttu-id="c1911-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1911-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c1911-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1911-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c1911-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1911-113">Methods</span></span>

<span data-ttu-id="c1911-114">A classe **MicrosoftDNS \_ ATMAType** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c1911-114">The **MicrosoftDNS\_ATMAType** class has these methods.</span></span>



| <span data-ttu-id="c1911-115">Método</span><span class="sxs-lookup"><span data-stu-id="c1911-115">Method</span></span>                             | <span data-ttu-id="c1911-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1911-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1911-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="c1911-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="c1911-118">Cria uma instância de um registro de recurso ATMA com base nos dados nos parâmetros de entrada do método: o nome do servidor DNS do registro, o nome do contêiner, o nome do proprietário/nó, a classe (padrão = IN), o valor de vida útil e o formato e o endereço ATM.</span><span class="sxs-lookup"><span data-stu-id="c1911-118">Instantiates an ATMA Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/Node Name, class (default = IN), time-to-live value, and ATM format and address.</span></span> <span data-ttu-id="c1911-119">Retorna uma referência ao novo objeto como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="c1911-119">Returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="c1911-120">Qualificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="c1911-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="c1911-121">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="c1911-121">**Modify**</span></span>                         | <span data-ttu-id="c1911-122">Atualiza o TTL, o formato e o endereço ATMA para os valores especificados como os parâmetros de entrada deste método.</span><span class="sxs-lookup"><span data-stu-id="c1911-122">Updates the TTL, Format and ATMA Address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="c1911-123">Se um novo valor para um parâmetro não for especificado, o valor atual do parâmetro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="c1911-123">If a new value for a parameter is not specified, the current value for the parameter is not changed.</span></span> <span data-ttu-id="c1911-124">O método retorna uma referência ao objeto modificado como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="c1911-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="c1911-125">Qualificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="c1911-125">Qualifiers: Implemented</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="c1911-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1911-126">Properties</span></span>

<span data-ttu-id="c1911-127">A classe **MicrosoftDNS \_ ATMAType** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1911-127">The **MicrosoftDNS\_ATMAType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1911-128">**ATMAddress**</span><span class="sxs-lookup"><span data-stu-id="c1911-128">**ATMAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1911-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1911-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1911-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1911-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1911-131">Cadeia de caracteres de comprimento variável de octetos que contém o endereço ATM do nó/proprietário ao qual esse RR pertence.</span><span class="sxs-lookup"><span data-stu-id="c1911-131">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="c1911-132">Os primeiros 4 bytes da matriz são usados para armazenar o tamanho da cadeia de caracteres do octeto.</span><span class="sxs-lookup"><span data-stu-id="c1911-132">The first 4 bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="c1911-133">O byte mais significativo é armazenado em byte 0.</span><span class="sxs-lookup"><span data-stu-id="c1911-133">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="c1911-134">**Formato**</span><span class="sxs-lookup"><span data-stu-id="c1911-134">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1911-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c1911-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c1911-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1911-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1911-137">Formato de endereço ATM.</span><span class="sxs-lookup"><span data-stu-id="c1911-137">ATM address format.</span></span> <span data-ttu-id="c1911-138">Os valores válidos são: 0 indicando o formato de endereço do sistema final (AESA) do ATM e 1 indicando o formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="c1911-138">Valid values are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1911-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1911-139">Requirements</span></span>



| <span data-ttu-id="c1911-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1911-140">Requirement</span></span> | <span data-ttu-id="c1911-141">Valor</span><span class="sxs-lookup"><span data-stu-id="c1911-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1911-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1911-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c1911-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c1911-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c1911-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1911-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c1911-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1911-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1911-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1911-146">Namespace</span></span><br/>                | <span data-ttu-id="c1911-147">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="c1911-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c1911-148">MOF</span><span class="sxs-lookup"><span data-stu-id="c1911-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1911-149"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1911-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1911-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1911-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1911-151">**Método CreateInstanceFromPropertyData da \_ classe ATMAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c1911-151">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c1911-152">**Método Modify da classe MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="c1911-152">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="c1911-153">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c1911-153">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





