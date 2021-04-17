---
description: Especifica o nível de proteção para conteúdo de vídeo.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: Estrutura de D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783707"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a><span data-ttu-id="39a6e-103">Estrutura de sinalizadores de \_ proteção do D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="39a6e-103">D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS structure</span></span>

<span data-ttu-id="39a6e-104">Especifica o nível de proteção para conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="39a6e-104">Specifies the protection level for video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a6e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39a6e-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a><span data-ttu-id="39a6e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="39a6e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="39a6e-107">**ProtectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="39a6e-107">**ProtectionEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="39a6e-108">Se 1, a proteção de conteúdo de vídeo está habilitada.</span><span class="sxs-lookup"><span data-stu-id="39a6e-108">If 1, video content protection is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="39a6e-109">**OverlayOrFullscreenRequired**</span><span class="sxs-lookup"><span data-stu-id="39a6e-109">**OverlayOrFullscreenRequired**</span></span>
</dt> <dd>

<span data-ttu-id="39a6e-110">Se for 1, o aplicativo exigirá que o vídeo seja exibido usando uma sobreposição de hardware ou o modo exclusivo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="39a6e-110">If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.</span></span>

</dd> <dt>

<span data-ttu-id="39a6e-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="39a6e-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="39a6e-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="39a6e-112">Reserved.</span></span> <span data-ttu-id="39a6e-113">Definir todos os bits como zero.</span><span class="sxs-lookup"><span data-stu-id="39a6e-113">Set all bits to zero.</span></span>

</dd> <dt>

<span data-ttu-id="39a6e-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="39a6e-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="39a6e-115">Use esse membro para acessar todos os bits na União.</span><span class="sxs-lookup"><span data-stu-id="39a6e-115">Use this member to access all of the bits in the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39a6e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39a6e-116">Requirements</span></span>



| <span data-ttu-id="39a6e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="39a6e-117">Requirement</span></span> | <span data-ttu-id="39a6e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="39a6e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39a6e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39a6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39a6e-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="39a6e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="39a6e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39a6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39a6e-122">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="39a6e-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39a6e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39a6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a6e-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="39a6e-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a6e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="39a6e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a6e-126">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="39a6e-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




