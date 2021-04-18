---
description: Indica o tipo de codificação usado.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Enumeração de CAPICOM_ENCODING_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756379"
---
# <a name="capicom_encoding_type-enumeration"></a><span data-ttu-id="21da8-103">Enumeração do tipo de \_ codificação CApicom \_</span><span class="sxs-lookup"><span data-stu-id="21da8-103">CAPICOM\_ENCODING\_TYPE enumeration</span></span>

<span data-ttu-id="21da8-104">O tipo de enumeração de **\_ \_ tipo de codificação capicor** indica o tipo de codificação usado.</span><span class="sxs-lookup"><span data-stu-id="21da8-104">The **CAPICOM\_ENCODING\_TYPE** enumeration type indicates the encoding type used.</span></span>

## <a name="members"></a><span data-ttu-id="21da8-105">Membros</span><span class="sxs-lookup"><span data-stu-id="21da8-105">Members</span></span>



| <span data-ttu-id="21da8-106">Membro</span><span class="sxs-lookup"><span data-stu-id="21da8-106">Member</span></span>                      | <span data-ttu-id="21da8-107">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="21da8-107">Description</span></span>                                                                                                                                                                                 | <span data-ttu-id="21da8-108">Valor</span><span class="sxs-lookup"><span data-stu-id="21da8-108">Value</span></span>      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="21da8-109">**CAPICOM \_ codificar \_ qualquer**</span><span class="sxs-lookup"><span data-stu-id="21da8-109">**CAPICOM\_ENCODE\_ANY**</span></span>    | <span data-ttu-id="21da8-110">Os dados são salvos como uma cadeia de caracteres codificada em base64 ou uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="21da8-110">Data is saved as a base64-encoded string or a pure binary sequence.</span></span> <span data-ttu-id="21da8-111">Esse tipo de codificação é usado somente para dados de entrada que têm um tipo de codificação desconhecido.</span><span class="sxs-lookup"><span data-stu-id="21da8-111">This encoding type is used only for input data that has an unknown encoding type.</span></span> <span data-ttu-id="21da8-112">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="21da8-112">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="21da8-113">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="21da8-113">0xffffffff</span></span> |
| <span data-ttu-id="21da8-114">**CAPICOM \_ codificar \_ Base64**</span><span class="sxs-lookup"><span data-stu-id="21da8-114">**CAPICOM\_ENCODE\_BASE64**</span></span> | <span data-ttu-id="21da8-115">Os dados são salvos como uma cadeia de caracteres codificada em base64.</span><span class="sxs-lookup"><span data-stu-id="21da8-115">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                        | <span data-ttu-id="21da8-116">0</span><span class="sxs-lookup"><span data-stu-id="21da8-116">0</span></span>          |
| <span data-ttu-id="21da8-117">**capicote de \_ codificação \_ binário**</span><span class="sxs-lookup"><span data-stu-id="21da8-117">**CAPICOM\_ENCODE\_BINARY**</span></span> | <span data-ttu-id="21da8-118">Os dados são salvos como uma sequência binária pura.</span><span class="sxs-lookup"><span data-stu-id="21da8-118">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                         | <span data-ttu-id="21da8-119">1</span><span class="sxs-lookup"><span data-stu-id="21da8-119">1</span></span>          |



## <a name="remarks"></a><span data-ttu-id="21da8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="21da8-120">Remarks</span></span>

<span data-ttu-id="21da8-121">Esse tipo de enumeração é usado pelos seguintes métodos e propriedades CAPICOM:</span><span class="sxs-lookup"><span data-stu-id="21da8-121">This enumeration type is used by the following CAPICOM methods and properties:</span></span>

-   <span data-ttu-id="21da8-122">Método [**Certificate. Export**](certificate-export.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-122">[**Certificate.Export**](certificate-export.md) method</span></span>
-   <span data-ttu-id="21da8-123">Propriedade [**EncodedData. Value**](encodeddata-value.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-123">[**EncodedData.Value**](encodeddata-value.md) property</span></span>
-   <span data-ttu-id="21da8-124">Método [**EncryptedData. Encrypt**](encrypteddata-encrypt.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-124">[**EncryptedData.Encrypt**](encrypteddata-encrypt.md) method</span></span>
-   <span data-ttu-id="21da8-125">Método [**EnvelopedData. Encrypt**](envelopeddata-encrypt.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-125">[**EnvelopedData.Encrypt**](envelopeddata-encrypt.md) method</span></span>
-   <span data-ttu-id="21da8-126">Propriedade [**Extended. Value**](extendedproperty-value.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-126">[**ExtendedProperty.Value**](extendedproperty-value.md) property</span></span>
-   <span data-ttu-id="21da8-127">Método [**SignedData. Sign**](signeddata-sign.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-127">[**SignedData.Sign**](signeddata-sign.md) method</span></span>
-   <span data-ttu-id="21da8-128">Método [**SignedData. cosign**](signeddata-cosign.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-128">[**SignedData.CoSign**](signeddata-cosign.md) method</span></span>
-   <span data-ttu-id="21da8-129">Método [**Store. Export**](store-export.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-129">[**Store.Export**](store-export.md) method</span></span>
-   <span data-ttu-id="21da8-130">Método [**Utilities. Getaleatório**](utilities-getrandom.md)</span><span class="sxs-lookup"><span data-stu-id="21da8-130">[**Utilities.GetRandom**](utilities-getrandom.md) method</span></span>

## <a name="requirements"></a><span data-ttu-id="21da8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21da8-131">Requirements</span></span>



| <span data-ttu-id="21da8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="21da8-132">Requirement</span></span> | <span data-ttu-id="21da8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="21da8-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21da8-134">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="21da8-134">Redistributable</span></span><br/> | <span data-ttu-id="21da8-135">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="21da8-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="21da8-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21da8-136">Header</span></span><br/>          | <dl> <span data-ttu-id="21da8-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="21da8-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 




