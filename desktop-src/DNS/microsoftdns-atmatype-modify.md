---
title: Método Modify da classe MicrosoftDNS_ATMAType
description: O método Modify atualiza um endereço ATM para um registro de recurso de nome (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modificar o método DNS
- Modificar o método DNS, MicrosoftDNS_ATMAType classe
- MicrosoftDNS_ATMAType classe de DNS, método Modify
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009380"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="8c2be-106">Método Modify da classe MicrosoftDNS \_ ATMAType</span><span class="sxs-lookup"><span data-stu-id="8c2be-106">Modify method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="8c2be-107">O método **Modify** atualiza um endereço ATM para um registro de recurso de nome (ATMA).</span><span class="sxs-lookup"><span data-stu-id="8c2be-107">The **Modify** method updates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2be-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c2be-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8c2be-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c2be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c2be-110">*TTL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c2be-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2be-111">Tempo, em segundos, que o RR pode ser armazenado em cache por um resolvedor de DNS.</span><span class="sxs-lookup"><span data-stu-id="8c2be-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8c2be-112">*Formato* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c2be-112">*Format* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2be-113">Formato de endereço ATM.</span><span class="sxs-lookup"><span data-stu-id="8c2be-113">ATM address format.</span></span> <span data-ttu-id="8c2be-114">Dois valores possíveis para o formato são: 0 indicando o formato de endereço do sistema final do ATM (AESA) e 1 indicando o formato E. 164.</span><span class="sxs-lookup"><span data-stu-id="8c2be-114">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="8c2be-115">*ATMAddress* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c2be-115">*ATMAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2be-116">Cadeia de caracteres de comprimento variável de octetos que contém o endereço ATM do nó/proprietário ao qual esse RR pertence.</span><span class="sxs-lookup"><span data-stu-id="8c2be-116">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="8c2be-117">Os primeiros quatro bytes da matriz são usados para armazenar o tamanho da cadeia de caracteres do octeto.</span><span class="sxs-lookup"><span data-stu-id="8c2be-117">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="8c2be-118">O byte mais significativo é armazenado em byte 0.</span><span class="sxs-lookup"><span data-stu-id="8c2be-118">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="8c2be-119">*RR* \[ out, ref\]</span><span class="sxs-lookup"><span data-stu-id="8c2be-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2be-120">Referência ao novo objeto.</span><span class="sxs-lookup"><span data-stu-id="8c2be-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c2be-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c2be-121">Return value</span></span>

<span data-ttu-id="8c2be-122">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8c2be-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c2be-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c2be-123">Remarks</span></span>

<span data-ttu-id="8c2be-124">Qualquer parâmetro não especificado permanece inalterado no registro modificado.</span><span class="sxs-lookup"><span data-stu-id="8c2be-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2be-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c2be-125">Requirements</span></span>



| <span data-ttu-id="8c2be-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c2be-126">Requirement</span></span> | <span data-ttu-id="8c2be-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8c2be-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2be-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c2be-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2be-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8c2be-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8c2be-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c2be-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2be-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c2be-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8c2be-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c2be-132">Namespace</span></span><br/>                | <span data-ttu-id="8c2be-133">\\MicrosoftDNS raiz</span><span class="sxs-lookup"><span data-stu-id="8c2be-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8c2be-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8c2be-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c2be-135"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c2be-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2be-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c2be-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2be-137">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="8c2be-137">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="8c2be-138">**Método CreateInstanceFromPropertyData da \_ classe ATMAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="8c2be-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8c2be-139">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="8c2be-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





