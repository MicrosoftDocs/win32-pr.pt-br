---
description: Define ou recupera o comprimento da chave.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Propriedade Algorithm. KeyLength
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761398"
---
# <a name="algorithmkeylength-property"></a><span data-ttu-id="fc6d3-103">Propriedade Algorithm. KeyLength</span><span class="sxs-lookup"><span data-stu-id="fc6d3-103">Algorithm.KeyLength property</span></span>

<span data-ttu-id="fc6d3-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="fc6d3-105">Em vez disso, use a [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="fc6d3-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fc6d3-106">A propriedade **KeyLength** define ou recupera o comprimento da chave.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-106">The **KeyLength** property sets or retrieves the length of the key.</span></span>

<span data-ttu-id="fc6d3-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6d3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc6d3-108">Syntax</span></span>


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a><span data-ttu-id="fc6d3-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fc6d3-109">Property value</span></span>

<span data-ttu-id="fc6d3-110">Um valor da enumeração [**de \_ \_ \_ comprimento da chave de criptografia capicor**](capicom-encryption-key-length.md) que especifica o comprimento da chave.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-110">A value of the [**CAPICOM\_ENCRYPTION\_KEY\_LENGTH**](capicom-encryption-key-length.md) enumeration that specifies the key length.</span></span> <span data-ttu-id="fc6d3-111">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="fc6d3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="fc6d3-112">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="fc6d3-113">Significado</span><span class="sxs-lookup"><span data-stu-id="fc6d3-113">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <span data-ttu-id="fc6d3-114"><dt>**\_ \_ \_ comprimento máximo da chave de criptografia CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc6d3-114"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</dt></span></span> </dl>     | <span data-ttu-id="fc6d3-115">Use o comprimento máximo de chave disponível com o algoritmo de criptografia indicado.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-115">Use the maximum key length available with the indicated encryption algorithm.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <span data-ttu-id="fc6d3-116"><dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 40 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="fc6d3-116"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="fc6d3-117">Use chaves de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-117">Use 40-bit keys.</span></span><br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <span data-ttu-id="fc6d3-118"><dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 56 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="fc6d3-118"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="fc6d3-119">Use chaves de 56 bits, se disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-119">Use 56-bit keys if available.</span></span><br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <span data-ttu-id="fc6d3-120"><dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 128 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="fc6d3-120"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</dt></span></span> </dl> | <span data-ttu-id="fc6d3-121">Use chaves de 128 bits, se disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-121">Use 128-bit keys if available.</span></span><br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <span data-ttu-id="fc6d3-122"><dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 192 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="fc6d3-122"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</dt></span></span> </dl> | <span data-ttu-id="fc6d3-123">Use chaves de 192 bits.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-123">Use 192-bit keys.</span></span> <span data-ttu-id="fc6d3-124">Esse comprimento de chave está disponível apenas para AES.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-124">This key length is available only for AES.</span></span><br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <span data-ttu-id="fc6d3-125"><dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 256 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="fc6d3-125"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</dt></span></span> </dl> | <span data-ttu-id="fc6d3-126">Use chaves de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-126">Use 256-bit keys.</span></span> <span data-ttu-id="fc6d3-127">Esse comprimento de chave está disponível apenas para AES.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-127">This key length is available only for AES.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fc6d3-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc6d3-128">Remarks</span></span>

<span data-ttu-id="fc6d3-129">Quando algoritmos de criptografia DES e 3DES são usados, os comprimentos de chave são padrão e a propriedade **KeyLength** é ignorada.</span><span class="sxs-lookup"><span data-stu-id="fc6d3-129">When DES and 3DES encryption algorithms are used, the key lengths are standard and the **KeyLength** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6d3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc6d3-130">Requirements</span></span>



| <span data-ttu-id="fc6d3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc6d3-131">Requirement</span></span> | <span data-ttu-id="fc6d3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="fc6d3-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6d3-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fc6d3-133">End of client support</span></span><br/> | <span data-ttu-id="fc6d3-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc6d3-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fc6d3-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="fc6d3-135">End of server support</span></span><br/> | <span data-ttu-id="fc6d3-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc6d3-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fc6d3-137">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="fc6d3-137">Redistributable</span></span><br/>       | <span data-ttu-id="fc6d3-138">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc6d3-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fc6d3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fc6d3-139">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fc6d3-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc6d3-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc6d3-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc6d3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6d3-142">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="fc6d3-142">**Algorithm**</span></span>](algorithm.md)
</dt> </dl>

 

 
