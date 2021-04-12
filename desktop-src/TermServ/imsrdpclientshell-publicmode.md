---
title: Propriedade IMsRdpClientShell Públicomode
description: Especifica ou recupera se o modo público está habilitado.
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade públicomode
- Propriedade publicmode Serviços de Área de Trabalho Remota, interface IMsRdpClientShell
- Serviços de Área de Trabalho Remota da interface IMsRdpClientShell, Propriedade Publicmode
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4129b3a9eeb62af0fa6e970c812ea6adf9670c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455494"
---
# <a name="imsrdpclientshellpublicmode-property"></a><span data-ttu-id="f98b1-106">IMsRdpClientShell: Propriedade ublicMode de:P</span><span class="sxs-lookup"><span data-stu-id="f98b1-106">IMsRdpClientShell::PublicMode property</span></span>

<span data-ttu-id="f98b1-107">Especifica ou recupera se o modo público está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f98b1-107">Specifies or retrieves whether public mode is enabled.</span></span>

<span data-ttu-id="f98b1-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f98b1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f98b1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f98b1-109">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="f98b1-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f98b1-110">Property value</span></span>

<span data-ttu-id="f98b1-111">Especifica se o modo público está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f98b1-111">Specifies whether public mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f98b1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f98b1-112">Requirements</span></span>



| <span data-ttu-id="f98b1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f98b1-113">Requirement</span></span> | <span data-ttu-id="f98b1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f98b1-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f98b1-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f98b1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f98b1-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f98b1-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f98b1-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f98b1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f98b1-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f98b1-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f98b1-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f98b1-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="f98b1-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f98b1-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f98b1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f98b1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f98b1-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f98b1-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f98b1-123">IID</span><span class="sxs-lookup"><span data-stu-id="f98b1-123">IID</span></span><br/>                      | <span data-ttu-id="f98b1-124">IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="f98b1-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f98b1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f98b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f98b1-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="f98b1-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





