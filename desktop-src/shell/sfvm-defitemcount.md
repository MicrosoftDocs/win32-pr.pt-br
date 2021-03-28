---
description: 'Permite que o objeto de retorno de chamada especifique o número de itens no modo de exibição de pasta. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_DEFITEMCOUNT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e3f746e422428ab9f925cf4ff3f460ccd578367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921976"
---
# <a name="sfvm_defitemcount-message"></a><span data-ttu-id="411c2-104">\_Mensagem SFVM DEFITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="411c2-104">SFVM\_DEFITEMCOUNT message</span></span>

<span data-ttu-id="411c2-105">Permite que o objeto de retorno de chamada especifique o número de itens no modo de exibição de pasta.</span><span class="sxs-lookup"><span data-stu-id="411c2-105">Allows the callback object to specify the number of items in the folder view.</span></span> <span data-ttu-id="411c2-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="411c2-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a><span data-ttu-id="411c2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="411c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="411c2-108">*cItems* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="411c2-108">*cItems* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="411c2-109">O número de itens na exibição de pasta.</span><span class="sxs-lookup"><span data-stu-id="411c2-109">The number of items in the folder view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="411c2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="411c2-110">Requirements</span></span>



| <span data-ttu-id="411c2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="411c2-111">Requirement</span></span> | <span data-ttu-id="411c2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="411c2-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="411c2-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="411c2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="411c2-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="411c2-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="411c2-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="411c2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="411c2-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="411c2-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="411c2-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="411c2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="411c2-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="411c2-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
