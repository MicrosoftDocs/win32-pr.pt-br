---
description: Contém um Message Authentication Code (MAC).
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: Estrutura de D3D_OMAC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766562"
---
# <a name="d3d_omac-structure"></a><span data-ttu-id="48fed-103">\_Estrutura OMAC do D3D</span><span class="sxs-lookup"><span data-stu-id="48fed-103">D3D\_OMAC structure</span></span>

<span data-ttu-id="48fed-104">Contém um Message Authentication Code (MAC).</span><span class="sxs-lookup"><span data-stu-id="48fed-104">Contains a Message Authentication Code (MAC).</span></span>

## <a name="syntax"></a><span data-ttu-id="48fed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48fed-105">Syntax</span></span>


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a><span data-ttu-id="48fed-106">Membros</span><span class="sxs-lookup"><span data-stu-id="48fed-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="48fed-107">**Omac**</span><span class="sxs-lookup"><span data-stu-id="48fed-107">**Omac**</span></span>
</dt> <dd>

<span data-ttu-id="48fed-108">Uma matriz de bytes que contém o valor de MAC criptográfico da mensagem.</span><span class="sxs-lookup"><span data-stu-id="48fed-108">A byte array that contains the cryptographic MAC value of the message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48fed-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48fed-109">Requirements</span></span>



| <span data-ttu-id="48fed-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="48fed-110">Requirement</span></span> | <span data-ttu-id="48fed-111">Valor</span><span class="sxs-lookup"><span data-stu-id="48fed-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48fed-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48fed-112">Minimum supported client</span></span><br/> | <span data-ttu-id="48fed-113">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="48fed-113">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="48fed-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48fed-114">Minimum supported server</span></span><br/> | <span data-ttu-id="48fed-115">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="48fed-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="48fed-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48fed-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="48fed-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="48fed-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48fed-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="48fed-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48fed-119">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="48fed-119">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




