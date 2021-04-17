---
description: Define ou recupera o algoritmo usado para as operações de assinatura, enveloping e criptografia. Essa é a propriedade padrão.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Propriedade Algorithm.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749464"
---
# <a name="algorithmname-property"></a><span data-ttu-id="56f4a-104">Propriedade Algorithm.Name</span><span class="sxs-lookup"><span data-stu-id="56f4a-104">Algorithm.Name property</span></span>

<span data-ttu-id="56f4a-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="56f4a-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="56f4a-106">Em vez disso, use a [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="56f4a-106">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="56f4a-107">A propriedade **Name** define ou recupera o algoritmo usado para as operações de assinatura, enveloping e criptografia.</span><span class="sxs-lookup"><span data-stu-id="56f4a-107">The **Name** property sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="56f4a-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="56f4a-108">This is the default property.</span></span>

<span data-ttu-id="56f4a-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="56f4a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f4a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="56f4a-110">Syntax</span></span>


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="56f4a-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="56f4a-111">Property value</span></span>

<span data-ttu-id="56f4a-112">Um valor da enumeração [**do \_ \_ algoritmo de criptografia capicor**](capicom-encryption-algorithm.md) que especifica qual algoritmo usar.</span><span class="sxs-lookup"><span data-stu-id="56f4a-112">A value of the [**CAPICOM\_ENCRYPTION\_ALGORITHM**](capicom-encryption-algorithm.md) enumeration that specifies which algorithm to use.</span></span> <span data-ttu-id="56f4a-113">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="56f4a-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="56f4a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="56f4a-114">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="56f4a-115">Significado</span><span class="sxs-lookup"><span data-stu-id="56f4a-115">Meaning</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <span data-ttu-id="56f4a-116"><dt>**Algoritmo de criptografia CAPICOM \_ \_ \_ RC2**</dt></span><span class="sxs-lookup"><span data-stu-id="56f4a-116"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</dt></span></span> </dl>    | <span data-ttu-id="56f4a-117">Use a criptografia RC2.</span><span class="sxs-lookup"><span data-stu-id="56f4a-117">Use RC2 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <span data-ttu-id="56f4a-118"><dt>**Algoritmo de criptografia capicor \_ \_ \_ RC4**</dt></span><span class="sxs-lookup"><span data-stu-id="56f4a-118"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</dt></span></span> </dl>    | <span data-ttu-id="56f4a-119">Use a criptografia RC4.</span><span class="sxs-lookup"><span data-stu-id="56f4a-119">Use RC4 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <span data-ttu-id="56f4a-120"><dt>**algoritmo de criptografia CAPICOM \_ \_ \_ des**</dt></span><span class="sxs-lookup"><span data-stu-id="56f4a-120"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</dt></span></span> </dl>    | <span data-ttu-id="56f4a-121">Use a criptografia DES.</span><span class="sxs-lookup"><span data-stu-id="56f4a-121">Use DES encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <span data-ttu-id="56f4a-122"><dt>**Algoritmo de criptografia CAPICOM \_ \_ \_ 3DES**</dt></span><span class="sxs-lookup"><span data-stu-id="56f4a-122"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</dt></span></span> </dl> | <span data-ttu-id="56f4a-123">Use a criptografia triple DES.</span><span class="sxs-lookup"><span data-stu-id="56f4a-123">Use triple DES encryption.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <span data-ttu-id="56f4a-124"><dt>**algoritmo de criptografia capicor \_ \_ \_ AES**</dt></span><span class="sxs-lookup"><span data-stu-id="56f4a-124"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</dt></span></span> </dl>    | <span data-ttu-id="56f4a-125">Use o algoritmo AES.</span><span class="sxs-lookup"><span data-stu-id="56f4a-125">Use the AES algorithm.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="56f4a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="56f4a-126">Remarks</span></span>

<span data-ttu-id="56f4a-127">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o estado inteiro do objeto é redefinido.</span><span class="sxs-lookup"><span data-stu-id="56f4a-127">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f4a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56f4a-128">Requirements</span></span>



| <span data-ttu-id="56f4a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="56f4a-129">Requirement</span></span> | <span data-ttu-id="56f4a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="56f4a-130">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56f4a-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="56f4a-131">End of client support</span></span><br/> | <span data-ttu-id="56f4a-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56f4a-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="56f4a-133">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="56f4a-133">End of server support</span></span><br/> | <span data-ttu-id="56f4a-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56f4a-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="56f4a-135">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="56f4a-135">Redistributable</span></span><br/>       | <span data-ttu-id="56f4a-136">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="56f4a-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="56f4a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="56f4a-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="56f4a-138"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56f4a-138"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
