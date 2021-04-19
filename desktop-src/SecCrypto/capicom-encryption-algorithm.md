---
description: Define os algoritmos a serem usados na criptografia e na descriptografia.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Enumeração de CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749211"
---
# <a name="capicom_encryption_algorithm-enumeration"></a><span data-ttu-id="6e117-103">Enumeração do algoritmo de \_ criptografia CApicom \_</span><span class="sxs-lookup"><span data-stu-id="6e117-103">CAPICOM\_ENCRYPTION\_ALGORITHM enumeration</span></span>

<span data-ttu-id="6e117-104">O tipo de enumeração do **\_ \_ algoritmo de criptografia capicor** define os algoritmos a serem usados na criptografia e na descriptografia.</span><span class="sxs-lookup"><span data-stu-id="6e117-104">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type defines the algorithms to be used in encryption and decryption.</span></span>

## <a name="members"></a><span data-ttu-id="6e117-105">Membros</span><span class="sxs-lookup"><span data-stu-id="6e117-105">Members</span></span>



| <span data-ttu-id="6e117-106">Membro</span><span class="sxs-lookup"><span data-stu-id="6e117-106">Member</span></span>                                   | <span data-ttu-id="6e117-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="6e117-107">Description</span></span>                                                                                                                                                                                              | <span data-ttu-id="6e117-108">Valor</span><span class="sxs-lookup"><span data-stu-id="6e117-108">Value</span></span>     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6e117-109">**Algoritmo de criptografia CAPICOM \_ \_ \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="6e117-109">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</span></span>  | <span data-ttu-id="6e117-110">Use a criptografia RSA RC2.</span><span class="sxs-lookup"><span data-stu-id="6e117-110">Use RSA RC2 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="6e117-111">0</span><span class="sxs-lookup"><span data-stu-id="6e117-111">0</span></span>         |
| <span data-ttu-id="6e117-112">**Algoritmo de criptografia capicor \_ \_ \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="6e117-112">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</span></span>  | <span data-ttu-id="6e117-113">Use a criptografia RSA RC4.</span><span class="sxs-lookup"><span data-stu-id="6e117-113">Use RSA RC4 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="6e117-114">1</span><span class="sxs-lookup"><span data-stu-id="6e117-114">1</span></span>         |
| <span data-ttu-id="6e117-115">**algoritmo de criptografia CAPICOM \_ \_ \_ des**</span><span class="sxs-lookup"><span data-stu-id="6e117-115">**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</span></span>  | <span data-ttu-id="6e117-116">Use a criptografia DES.</span><span class="sxs-lookup"><span data-stu-id="6e117-116">Use DES encryption.</span></span><br/>                                                                                                                                                                           | <span data-ttu-id="6e117-117">2</span><span class="sxs-lookup"><span data-stu-id="6e117-117">2</span></span>         |
| <span data-ttu-id="6e117-118">**Algoritmo de criptografia CAPICOM \_ \_ \_ 3DES**</span><span class="sxs-lookup"><span data-stu-id="6e117-118">**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</span></span> | <span data-ttu-id="6e117-119">Use a criptografia triple DES.</span><span class="sxs-lookup"><span data-stu-id="6e117-119">Use triple DES encryption.</span></span><br/>                                                                                                                                                                    | <span data-ttu-id="6e117-120">3</span><span class="sxs-lookup"><span data-stu-id="6e117-120">3</span></span>         |
| <span data-ttu-id="6e117-121">**algoritmo de criptografia capicor \_ \_ \_ AES**</span><span class="sxs-lookup"><span data-stu-id="6e117-121">**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</span></span>  | <span data-ttu-id="6e117-122">Use o algoritmo [*criptografia AES*](../secgloss/a-gly.md) (AES).</span><span class="sxs-lookup"><span data-stu-id="6e117-122">Use the [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) algorithm.</span></span> <span data-ttu-id="6e117-123">Esse valor é válido somente para o objeto [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="6e117-123">This value is valid for the [**EncryptedData**](encrypteddata.md) object only.</span></span><br/> | <span data-ttu-id="6e117-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="6e117-124">4 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="6e117-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e117-125">Remarks</span></span>

<span data-ttu-id="6e117-126">O tipo de enumeração de **\_ \_ algoritmo de criptografia capicor** é usado pela propriedade [**Algorithm.Name**](algorithm-name.md) .</span><span class="sxs-lookup"><span data-stu-id="6e117-126">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type is used by the [**Algorithm.Name**](algorithm-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e117-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e117-127">Requirements</span></span>



| <span data-ttu-id="6e117-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e117-128">Requirement</span></span> | <span data-ttu-id="6e117-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6e117-129">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e117-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6e117-130">Redistributable</span></span><br/> | <span data-ttu-id="6e117-131">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e117-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="6e117-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e117-132">Header</span></span><br/>          | <dl> <span data-ttu-id="6e117-133"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e117-133"><dt>Capicom.h</dt></span></span> </dl> |



 

 
