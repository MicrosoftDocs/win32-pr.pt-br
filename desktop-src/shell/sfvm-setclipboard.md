---
description: Notifica o IShellView quando um de seus objetos é colocado na área de transferência como resultado de um comando de menu. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_SETCLIPBOARD (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989102"
---
# <a name="sfvm_setclipboard-message"></a><span data-ttu-id="01130-104">SFVM \_ mensagem da área de transferência</span><span class="sxs-lookup"><span data-stu-id="01130-104">SFVM\_SETCLIPBOARD message</span></span>

<span data-ttu-id="01130-105">Notifica o [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) quando um de seus objetos é colocado na área de transferência como resultado de um comando de menu.</span><span class="sxs-lookup"><span data-stu-id="01130-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) when one of its objects is placed on the Clipboard as a result of a menu command.</span></span> <span data-ttu-id="01130-106">Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="01130-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a><span data-ttu-id="01130-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01130-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01130-108">*dwEffect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01130-108">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01130-109">Use (WPARAM)-2 se o item estiver sendo recortado para a área de transferência ou (WPARAM)-3 se o item estiver sendo copiado para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="01130-109">Use (WPARAM)-2 if the item is being cut to the Clipboard or (WPARAM)-3 if the item is being copied to the Clipboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01130-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01130-110">Return value</span></span>

<span data-ttu-id="01130-111">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="01130-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01130-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="01130-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="01130-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01130-113">Requirements</span></span>



| <span data-ttu-id="01130-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="01130-114">Requirement</span></span> | <span data-ttu-id="01130-115">Valor</span><span class="sxs-lookup"><span data-stu-id="01130-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01130-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01130-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01130-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01130-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="01130-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01130-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01130-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01130-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="01130-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="01130-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01130-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="01130-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




