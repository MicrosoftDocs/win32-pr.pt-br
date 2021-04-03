---
title: Propriedade IMsRdpClientNonScriptable5 GetRemoteMonitorsBoundingBox
description: Especifica o retângulo delimitador do monitor remoto.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GetRemoteMonitorsBoundingBox
- Propriedade GetRemoteMonitorsBoundingBox Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade GetRemoteMonitorsBoundingBox
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918738"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a><span data-ttu-id="07e8b-106">Propriedade IMsRdpClientNonScriptable5:: GetRemoteMonitorsBoundingBox</span><span class="sxs-lookup"><span data-stu-id="07e8b-106">IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox property</span></span>

<span data-ttu-id="07e8b-107">Especifica o retângulo delimitador do monitor remoto.</span><span class="sxs-lookup"><span data-stu-id="07e8b-107">Specifies the bounding rectangle of the remote monitor.</span></span>

<span data-ttu-id="07e8b-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="07e8b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e8b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07e8b-109">Syntax</span></span>


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a><span data-ttu-id="07e8b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="07e8b-110">Property value</span></span>

<span data-ttu-id="07e8b-111">Recebe a borda esquerda do retângulo.</span><span class="sxs-lookup"><span data-stu-id="07e8b-111">Receives the left edge of the rectangle.</span></span>

<span data-ttu-id="07e8b-112">Recebe a borda superior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="07e8b-112">Receives the top edge of the rectangle.</span></span>

<span data-ttu-id="07e8b-113">Recebe a borda direita do retângulo.</span><span class="sxs-lookup"><span data-stu-id="07e8b-113">Receives the right edge of the rectangle.</span></span>

<span data-ttu-id="07e8b-114">Recebe a borda inferior do retângulo.</span><span class="sxs-lookup"><span data-stu-id="07e8b-114">Receives the bottom edge of the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="07e8b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="07e8b-115">Remarks</span></span>

<span data-ttu-id="07e8b-116">Todas as coordenadas estão em coordenadas de tela virtual, que são relativas ao canto superior esquerdo do monitor primário.</span><span class="sxs-lookup"><span data-stu-id="07e8b-116">All coordinates are in virtual screen coordinates, which are relative to the upper-left corner of the primary monitor.</span></span> <span data-ttu-id="07e8b-117">Se esse não for o monitor primário, alguns ou todos esses valores poderão ser negativos.</span><span class="sxs-lookup"><span data-stu-id="07e8b-117">If this is not the primary monitor, some or all of these values may be negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="07e8b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07e8b-118">Requirements</span></span>



| <span data-ttu-id="07e8b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="07e8b-119">Requirement</span></span> | <span data-ttu-id="07e8b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="07e8b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07e8b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07e8b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="07e8b-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07e8b-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="07e8b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07e8b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="07e8b-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="07e8b-124">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="07e8b-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="07e8b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="07e8b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07e8b-126"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="07e8b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="07e8b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07e8b-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07e8b-128"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="07e8b-129">IID</span><span class="sxs-lookup"><span data-stu-id="07e8b-129">IID</span></span><br/>                      | <span data-ttu-id="07e8b-130">IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="07e8b-130">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07e8b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="07e8b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e8b-132">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="07e8b-132">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





