---
description: Especifica quais bytes são criptografados em uma superfície de vídeo protegida.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: Estrutura de D3DENCRYPTED_BLOCK_INFO (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089755"
---
# <a name="d3dencrypted_block_info-structure"></a><span data-ttu-id="bdab7-103">Estrutura de informações de \_ bloco D3DENCRYPTED \_</span><span class="sxs-lookup"><span data-stu-id="bdab7-103">D3DENCRYPTED\_BLOCK\_INFO structure</span></span>

<span data-ttu-id="bdab7-104">Especifica quais bytes são criptografados em uma superfície de vídeo protegida.</span><span class="sxs-lookup"><span data-stu-id="bdab7-104">Specifies which bytes are encrypted in a protected video surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdab7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdab7-105">Syntax</span></span>


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a><span data-ttu-id="bdab7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="bdab7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bdab7-107">**NumEncryptedBytesAtBeginning**</span><span class="sxs-lookup"><span data-stu-id="bdab7-107">**NumEncryptedBytesAtBeginning**</span></span>
</dt> <dd>

<span data-ttu-id="bdab7-108">O número de bytes que são criptografados no início do buffer.</span><span class="sxs-lookup"><span data-stu-id="bdab7-108">The number of bytes that are encrypted at the start of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bdab7-109">**NumBytesInSkipPattern**</span><span class="sxs-lookup"><span data-stu-id="bdab7-109">**NumBytesInSkipPattern**</span></span>
</dt> <dd>

<span data-ttu-id="bdab7-110">O número de bytes que são ignorados após os primeiros **NumEncryptedBytesAtBeginning** bytes e depois de cada bloco de **NumBytesInEncryptPattern** bytes.</span><span class="sxs-lookup"><span data-stu-id="bdab7-110">The number of bytes that are skipped after the first **NumEncryptedBytesAtBeginning** bytes, and then after each block of **NumBytesInEncryptPattern** bytes.</span></span> <span data-ttu-id="bdab7-111">Bytes ignorados não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="bdab7-111">Skipped bytes are not encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="bdab7-112">**NumBytesInEncryptPattern**</span><span class="sxs-lookup"><span data-stu-id="bdab7-112">**NumBytesInEncryptPattern**</span></span>
</dt> <dd>

<span data-ttu-id="bdab7-113">O número de bytes que são criptografados após cada bloco de bytes ignorados.</span><span class="sxs-lookup"><span data-stu-id="bdab7-113">The number of bytes that are encrypted after each block of skipped bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bdab7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdab7-114">Requirements</span></span>



| <span data-ttu-id="bdab7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdab7-115">Requirement</span></span> | <span data-ttu-id="bdab7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bdab7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdab7-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdab7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bdab7-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bdab7-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bdab7-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdab7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bdab7-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bdab7-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bdab7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdab7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdab7-122"><dt>D3d9types. h (incluir D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdab7-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdab7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdab7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdab7-124">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="bdab7-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




