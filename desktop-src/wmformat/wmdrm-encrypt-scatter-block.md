---
title: Estrutura de WMDRM_ENCRYPT_SCATTER_BLOCK (wmdrmsdk. h)
description: A \_ \_ \_ estrutura de bloco de dispersão de criptografia WMDRM contém um bloco de dados a ser criptografado.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_ENCRYPT_SCATTER_BLOCK
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788791"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a><span data-ttu-id="92b6e-105">\_Estrutura de \_ bloco de dispersas do WMDRM Encrypt \_</span><span class="sxs-lookup"><span data-stu-id="92b6e-105">WMDRM\_ENCRYPT\_SCATTER\_BLOCK structure</span></span>

<span data-ttu-id="92b6e-106">A estrutura de **\_ \_ \_ bloco de dispersão de criptografia WMDRM** contém um bloco de dados a ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="92b6e-106">The **WMDRM\_ENCRYPT\_SCATTER\_BLOCK** structure contains a block of data to be encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b6e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92b6e-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a><span data-ttu-id="92b6e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="92b6e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="92b6e-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="92b6e-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="92b6e-110">Identificador do fluxo ao qual o bloco de dados pertence.</span><span class="sxs-lookup"><span data-stu-id="92b6e-110">Identifier of the stream to which the data block belongs.</span></span>

</dd> <dt>

<span data-ttu-id="92b6e-111">**cbBlock**</span><span class="sxs-lookup"><span data-stu-id="92b6e-111">**cbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="92b6e-112">Tamanho do bloco em bytes.</span><span class="sxs-lookup"><span data-stu-id="92b6e-112">Size of block in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="92b6e-113">**pbBlock**</span><span class="sxs-lookup"><span data-stu-id="92b6e-113">**pbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="92b6e-114">Ponteiro para um buffer que contém o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="92b6e-114">Pointer to a buffer containing the data block.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92b6e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="92b6e-115">Remarks</span></span>

<span data-ttu-id="92b6e-116">Essa estrutura é usada pelo método [**IWMDRMEncryptScatter:: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) para identificar blocos de dados a serem criptografados.</span><span class="sxs-lookup"><span data-stu-id="92b6e-116">This structure is used by the [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) method to identify blocks of data to encrypt.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b6e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92b6e-117">Requirements</span></span>



| <span data-ttu-id="92b6e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b6e-118">Requirement</span></span> | <span data-ttu-id="92b6e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="92b6e-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92b6e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92b6e-120">Header</span></span><br/> | <dl> <span data-ttu-id="92b6e-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b6e-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b6e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="92b6e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b6e-123">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="92b6e-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





