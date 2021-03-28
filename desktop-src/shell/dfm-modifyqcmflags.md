---
description: 'Permite que o retorno de chamada modifique os valores do CFM \_ xxx passados para IContextMenu:: QueryContextMenu.'
title: Mensagem de DFM_MODIFYQCMFLAGS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826891"
---
# <a name="dfm_modifyqcmflags-message"></a><span data-ttu-id="ab704-103">\_Mensagem DFM MODIFYQCMFLAGS</span><span class="sxs-lookup"><span data-stu-id="ab704-103">DFM\_MODIFYQCMFLAGS message</span></span>

<span data-ttu-id="ab704-104">Permite que o retorno de chamada modifique os valores do CFM \_ xxx passados para [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="ab704-104">Allows the callback to modify the CFM\_XXX values passed to [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="ab704-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab704-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab704-106">*puNewFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab704-106">*puNewFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab704-107">Um ponteiro para os novos valores de sinalizador.</span><span class="sxs-lookup"><span data-stu-id="ab704-107">A pointer to the new flag values.</span></span>

</dd> <dt>

<span data-ttu-id="ab704-108">*uFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab704-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab704-109">Sinalizadores que especificam como o menu de contexto pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="ab704-109">Flags that specify how the context menu can be changed.</span></span> <span data-ttu-id="ab704-110">Esse parâmetro usa os valores de CMF \_ xxx descritos em [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="ab704-110">This parameter uses the CMF\_XXX values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab704-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab704-111">Requirements</span></span>



| <span data-ttu-id="ab704-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab704-112">Requirement</span></span> | <span data-ttu-id="ab704-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ab704-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab704-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab704-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ab704-115">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ab704-115">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ab704-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab704-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ab704-117">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ab704-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab704-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab704-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab704-119"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab704-119"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




