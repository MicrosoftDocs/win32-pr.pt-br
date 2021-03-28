---
description: Notifica o IShellView para reorganizar seus itens. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_REARRANGE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011776"
---
# <a name="sfvm_rearrange-message"></a><span data-ttu-id="e96fc-104">SFVM \_ reorganizar mensagem</span><span class="sxs-lookup"><span data-stu-id="e96fc-104">SFVM\_REARRANGE message</span></span>

<span data-ttu-id="e96fc-105">Notifica o [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) para reorganizar seus itens.</span><span class="sxs-lookup"><span data-stu-id="e96fc-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) to rearrange its items.</span></span> <span data-ttu-id="e96fc-106">Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="e96fc-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a><span data-ttu-id="e96fc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e96fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e96fc-108">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e96fc-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e96fc-109">Passado para [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span><span class="sxs-lookup"><span data-stu-id="e96fc-109">Passed to [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span></span> <span data-ttu-id="e96fc-110">Consulte [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) para obter mais informações sobre esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e96fc-110">See [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) for more information on this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e96fc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e96fc-111">Return value</span></span>

<span data-ttu-id="e96fc-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e96fc-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e96fc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e96fc-113">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e96fc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e96fc-114">Requirements</span></span>



| <span data-ttu-id="e96fc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e96fc-115">Requirement</span></span> | <span data-ttu-id="e96fc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e96fc-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e96fc-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e96fc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e96fc-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e96fc-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e96fc-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e96fc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e96fc-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e96fc-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e96fc-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e96fc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e96fc-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e96fc-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




