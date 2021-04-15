---
description: Define o comprimento da chave a ser usada na criptografia.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Enumeração de CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753721"
---
# <a name="capicom_encryption_key_length-enumeration"></a><span data-ttu-id="194fa-103">\_Enumeração de \_ comprimento de chave de criptografia CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="194fa-103">CAPICOM\_ENCRYPTION\_KEY\_LENGTH enumeration</span></span>

<span data-ttu-id="194fa-104">O tipo de enumeração de **comprimento da chave de \_ criptografia \_ \_ capicor** define o [*comprimento da chave*](../secgloss/k-gly.md) a ser usada na criptografia.</span><span class="sxs-lookup"><span data-stu-id="194fa-104">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type defines the [*key length*](../secgloss/k-gly.md) to be used in encryption.</span></span>

## <a name="members"></a><span data-ttu-id="194fa-105">Membros</span><span class="sxs-lookup"><span data-stu-id="194fa-105">Members</span></span>



| <span data-ttu-id="194fa-106">Membro</span><span class="sxs-lookup"><span data-stu-id="194fa-106">Member</span></span>                                          | <span data-ttu-id="194fa-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="194fa-107">Description</span></span>                                                                               | <span data-ttu-id="194fa-108">Valor</span><span class="sxs-lookup"><span data-stu-id="194fa-108">Value</span></span>     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="194fa-109">**\_ \_ \_ comprimento máximo da chave de criptografia CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="194fa-109">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</span></span>   | <span data-ttu-id="194fa-110">Usa o comprimento máximo de chave disponível com o algoritmo de criptografia indicado.</span><span class="sxs-lookup"><span data-stu-id="194fa-110">Uses the maximum key length available with the indicated encryption algorithm.</span></span><br/> | <span data-ttu-id="194fa-111">0</span><span class="sxs-lookup"><span data-stu-id="194fa-111">0</span></span>         |
| <span data-ttu-id="194fa-112">**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 40 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="194fa-112">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</span></span>  | <span data-ttu-id="194fa-113">Usa chaves de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="194fa-113">Uses 40-bit keys.</span></span><br/>                                                              | <span data-ttu-id="194fa-114">1</span><span class="sxs-lookup"><span data-stu-id="194fa-114">1</span></span>         |
| <span data-ttu-id="194fa-115">**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 56 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="194fa-115">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</span></span>  | <span data-ttu-id="194fa-116">Usa chaves de 56 bits, se disponíveis.</span><span class="sxs-lookup"><span data-stu-id="194fa-116">Uses 56-bit keys if available.</span></span><br/>                                                 | <span data-ttu-id="194fa-117">2</span><span class="sxs-lookup"><span data-stu-id="194fa-117">2</span></span>         |
| <span data-ttu-id="194fa-118">**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 128 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="194fa-118">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</span></span> | <span data-ttu-id="194fa-119">Usa chaves de 128 bits, se disponíveis.</span><span class="sxs-lookup"><span data-stu-id="194fa-119">Uses 128-bit keys if available.</span></span><br/>                                                | <span data-ttu-id="194fa-120">3</span><span class="sxs-lookup"><span data-stu-id="194fa-120">3</span></span>         |
| <span data-ttu-id="194fa-121">**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 192 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="194fa-121">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</span></span> | <span data-ttu-id="194fa-122">Usa chaves de 192 bits.</span><span class="sxs-lookup"><span data-stu-id="194fa-122">Uses 192-bit keys.</span></span> <span data-ttu-id="194fa-123">Esse comprimento de chave está disponível apenas para AES.</span><span class="sxs-lookup"><span data-stu-id="194fa-123">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="194fa-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="194fa-124">4 // v2.0</span></span> |
| <span data-ttu-id="194fa-125">**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 256 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="194fa-125">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</span></span> | <span data-ttu-id="194fa-126">Usa chaves de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="194fa-126">Uses 256-bit keys.</span></span> <span data-ttu-id="194fa-127">Esse comprimento de chave está disponível apenas para AES.</span><span class="sxs-lookup"><span data-stu-id="194fa-127">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="194fa-128">5//v 2.0</span><span class="sxs-lookup"><span data-stu-id="194fa-128">5 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="194fa-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="194fa-129">Remarks</span></span>

<span data-ttu-id="194fa-130">O tipo de enumeração de **\_ comprimento da \_ chave \_ de criptografia capicor** é usado pelo [**algoritmo. Propriedade KeyLength**](algorithm-keylength.md) .</span><span class="sxs-lookup"><span data-stu-id="194fa-130">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type is used by the [**Algorithm.KeyLength**](algorithm-keylength.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="194fa-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="194fa-131">Requirements</span></span>



| <span data-ttu-id="194fa-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="194fa-132">Requirement</span></span> | <span data-ttu-id="194fa-133">Valor</span><span class="sxs-lookup"><span data-stu-id="194fa-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="194fa-134">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="194fa-134">Redistributable</span></span><br/> | <span data-ttu-id="194fa-135">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="194fa-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="194fa-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="194fa-136">Header</span></span><br/>          | <dl> <span data-ttu-id="194fa-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="194fa-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 
