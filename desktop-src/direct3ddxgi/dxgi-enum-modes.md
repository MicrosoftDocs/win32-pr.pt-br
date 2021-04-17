---
description: Opções para enumeração de modos de exibição.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105754087"
---
# <a name="dxgi_enum_modes"></a><span data-ttu-id="e96a6-103">\_modos de enumeração dxgi \_</span><span class="sxs-lookup"><span data-stu-id="e96a6-103">DXGI\_ENUM\_MODES</span></span>

<span data-ttu-id="e96a6-104">Opções para enumeração de modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="e96a6-104">Options for enumerating display modes.</span></span>



| <span data-ttu-id="e96a6-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e96a6-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="e96a6-106">Description</span><span class="sxs-lookup"><span data-stu-id="e96a6-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <span data-ttu-id="e96a6-107"><dt>**Dxgi \_ Modos de enumeração \_ \_ entrelaçados**</dt> <dt>1UL</dt></span><span class="sxs-lookup"><span data-stu-id="e96a6-107"><dt>**DXGI\_ENUM\_MODES\_INTERLACED**</dt> <dt>1UL</dt></span></span> </dl>                 | <span data-ttu-id="e96a6-108">Incluir modos entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="e96a6-108">Include interlaced modes.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <span data-ttu-id="e96a6-109"><dt>**Dxgi \_ 2UL \_ de \_ dimensionamento de modos de enumeração**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e96a6-109"><dt>**DXGI\_ENUM\_MODES\_SCALING**</dt> <dt>2UL</dt></span></span> </dl>                          | <span data-ttu-id="e96a6-110">Incluir modos de dimensionamento ampliado.</span><span class="sxs-lookup"><span data-stu-id="e96a6-110">Include stretched-scaling modes.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <span data-ttu-id="e96a6-111"><dt>**Dxgi \_ Modos de enumeração 4UL \_ \_ estéreo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e96a6-111"><dt>**DXGI\_ENUM\_MODES\_STEREO**</dt> <dt>4UL</dt></span></span> </dl>                             | <span data-ttu-id="e96a6-112">Incluir modos estéreo.</span><span class="sxs-lookup"><span data-stu-id="e96a6-112">Include stereo modes.</span></span><br/> <span data-ttu-id="e96a6-113">**Direct3D 11:** Esse valor de enumeração tem suporte a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e96a6-113">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <span data-ttu-id="e96a6-114"><dt>**Dxgi \_ Modos de enumeração \_ \_ desabilitados 8UL \_ estéreo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e96a6-114"><dt>**DXGI\_ENUM\_MODES\_DISABLED\_STEREO**</dt> <dt>8UL</dt></span></span> </dl> | <span data-ttu-id="e96a6-115">Incluir modos estéreo ocultos porque o usuário desabilitou o estéreo.</span><span class="sxs-lookup"><span data-stu-id="e96a6-115">Include stereo modes that are hidden because the user has disabled stereo.</span></span> <span data-ttu-id="e96a6-116">Os aplicativos do painel de controle podem usar essa opção para mostrar os recursos de estéreo que foram desabilitados como parte de uma interface do usuário que habilita e desabilita o estéreo.</span><span class="sxs-lookup"><span data-stu-id="e96a6-116">Control panel applications can use this option to show stereo capabilities that have been disabled as part of a user interface that enables and disables stereo.</span></span><br/> <span data-ttu-id="e96a6-117">**Direct3D 11:** Esse valor de enumeração tem suporte a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e96a6-117">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e96a6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e96a6-118">Remarks</span></span>

<span data-ttu-id="e96a6-119">Essas opções de sinalizador são usadas em [**IDXGIOutput:: Getdisplaymodelist**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) para enumerar os modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="e96a6-119">These flag options are used in [**IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) to enumerate display modes.</span></span>

<span data-ttu-id="e96a6-120">Essas opções de sinalizador também são usadas em [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) para enumerar modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="e96a6-120">These flag options are also used in [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) to enumerate display modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="e96a6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e96a6-121">Requirements</span></span>



| <span data-ttu-id="e96a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e96a6-122">Requirement</span></span> | <span data-ttu-id="e96a6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e96a6-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e96a6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e96a6-124">Header</span></span><br/> | <dl> <span data-ttu-id="e96a6-125"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e96a6-125"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e96a6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e96a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e96a6-127">Constantes DXGI</span><span class="sxs-lookup"><span data-stu-id="e96a6-127">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




