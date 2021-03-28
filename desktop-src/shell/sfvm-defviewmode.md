---
description: 'Permite que o objeto de retorno de chamada especifique o modo de exibição. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_DEFVIEWMODE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8d57bb61b2b938947d0290345215e3735d9d8763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989090"
---
# <a name="sfvm_defviewmode-message"></a><span data-ttu-id="fc62d-104">\_Mensagem SFVM DEFVIEWMODE</span><span class="sxs-lookup"><span data-stu-id="fc62d-104">SFVM\_DEFVIEWMODE message</span></span>

<span data-ttu-id="fc62d-105">Permite que o objeto de retorno de chamada especifique o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="fc62d-105">Allows the callback object to specify the view mode.</span></span> <span data-ttu-id="fc62d-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="fc62d-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a><span data-ttu-id="fc62d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc62d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc62d-108">*pViewMode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fc62d-108">*pViewMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc62d-109">Um dos valores do tipo enumerado [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) .</span><span class="sxs-lookup"><span data-stu-id="fc62d-109">One of the values from the [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) enumerated type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc62d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc62d-110">Requirements</span></span>



| <span data-ttu-id="fc62d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc62d-111">Requirement</span></span> | <span data-ttu-id="fc62d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="fc62d-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fc62d-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc62d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fc62d-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc62d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fc62d-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc62d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fc62d-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc62d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fc62d-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fc62d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc62d-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc62d-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
