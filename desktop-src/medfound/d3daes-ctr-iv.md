---
description: Contém um vetor de inicialização (IV) para CTR de 128 bits criptografia AES modo de criptografia de codificação de bloco (AES-CTR).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: Estrutura de D3DAES_CTR_IV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296157"
---
# <a name="d3daes_ctr_iv-structure"></a><span data-ttu-id="81fcc-103">\_Estrutura D3DAES CTR \_ IV</span><span class="sxs-lookup"><span data-stu-id="81fcc-103">D3DAES\_CTR\_IV structure</span></span>

<span data-ttu-id="81fcc-104">Contém um vetor de inicialização (IV) para CTR de 128 bits criptografia AES modo de criptografia de codificação de bloco (AES-CTR).</span><span class="sxs-lookup"><span data-stu-id="81fcc-104">Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="81fcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81fcc-105">Syntax</span></span>


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a><span data-ttu-id="81fcc-106">Membros</span><span class="sxs-lookup"><span data-stu-id="81fcc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="81fcc-107">**IV**</span><span class="sxs-lookup"><span data-stu-id="81fcc-107">**IV**</span></span>
</dt> <dd>

<span data-ttu-id="81fcc-108">O IV, no formato big-endian.</span><span class="sxs-lookup"><span data-stu-id="81fcc-108">The IV, in big-endian format.</span></span>

</dd> <dt>

<span data-ttu-id="81fcc-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="81fcc-109">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="81fcc-110">A contagem de blocos, no formato big-endian.</span><span class="sxs-lookup"><span data-stu-id="81fcc-110">The block count, in big-endian format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81fcc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="81fcc-111">Remarks</span></span>

<span data-ttu-id="81fcc-112">A estrutura **D3DAES \_ CTR \_ IV** e a estrutura [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="81fcc-112">The **D3DAES\_CTR\_IV** structure and the [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) structure are equivalent.</span></span>

<span data-ttu-id="81fcc-113">Para obter detalhes, consulte [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span><span class="sxs-lookup"><span data-stu-id="81fcc-113">For details, see [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span></span>

## <a name="requirements"></a><span data-ttu-id="81fcc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81fcc-114">Requirements</span></span>



| <span data-ttu-id="81fcc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="81fcc-115">Requirement</span></span> | <span data-ttu-id="81fcc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="81fcc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fcc-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81fcc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81fcc-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="81fcc-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81fcc-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81fcc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81fcc-120">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="81fcc-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="81fcc-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81fcc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="81fcc-122"><dt>D3d9types. h (incluir D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81fcc-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81fcc-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="81fcc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81fcc-124">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="81fcc-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




