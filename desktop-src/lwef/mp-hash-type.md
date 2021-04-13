---
title: Enumeração de MP_HASH_TYPE (MpClient. h)
description: Tipos de hash possíveis.
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- Recursos do ambiente Windows herdado de enumeração de MP_HASH_TYPE
- PMP_HASH_TYPE recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455823"
---
# <a name="mp_hash_type-enumeration"></a><span data-ttu-id="61499-105">Enumeração de tipo de \_ hash MP \_</span><span class="sxs-lookup"><span data-stu-id="61499-105">MP\_HASH\_TYPE enumeration</span></span>

<span data-ttu-id="61499-106">Tipos de hash possíveis.</span><span class="sxs-lookup"><span data-stu-id="61499-106">Possible hash types.</span></span>

## <a name="syntax"></a><span data-ttu-id="61499-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="61499-107">Syntax</span></span>


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="61499-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="61499-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61499-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**\_tipo de hash MP \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="61499-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP\_HASH\_TYPE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="61499-110">Sem hash.</span><span class="sxs-lookup"><span data-stu-id="61499-110">No hash.</span></span>

</dd> <dt>

<span data-ttu-id="61499-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**\_Tipo de hash MP \_ \_ CRC32**</span><span class="sxs-lookup"><span data-stu-id="61499-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP\_HASH\_TYPE\_CRC32**</span></span>
</dt> <dd>

<span data-ttu-id="61499-112">CRC32</span><span class="sxs-lookup"><span data-stu-id="61499-112">CRC32</span></span>

</dd> <dt>

<span data-ttu-id="61499-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**\_Tipo de hash MP \_ \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="61499-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP\_HASH\_TYPE\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="61499-114">MD5</span><span class="sxs-lookup"><span data-stu-id="61499-114">MD5</span></span>

</dd> <dt>

<span data-ttu-id="61499-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**\_Tipo de hash MP \_ \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="61499-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP\_HASH\_TYPE\_SHA1**</span></span>
</dt> <dd>

<span data-ttu-id="61499-116">SHA1</span><span class="sxs-lookup"><span data-stu-id="61499-116">SHA1</span></span>

</dd> <dt>

<span data-ttu-id="61499-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**\_Tipo de hash MP \_ \_ SHA256**</span><span class="sxs-lookup"><span data-stu-id="61499-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP\_HASH\_TYPE\_SHA256**</span></span>
</dt> <dd>

<span data-ttu-id="61499-118">SHA 256</span><span class="sxs-lookup"><span data-stu-id="61499-118">SHA 256</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61499-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61499-119">Requirements</span></span>



| <span data-ttu-id="61499-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="61499-120">Requirement</span></span> | <span data-ttu-id="61499-121">Valor</span><span class="sxs-lookup"><span data-stu-id="61499-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61499-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61499-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61499-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61499-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="61499-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61499-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61499-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61499-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61499-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61499-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="61499-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="61499-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





