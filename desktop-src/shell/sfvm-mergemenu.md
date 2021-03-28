---
description: 'Permite que o objeto de retorno de chamada mescle itens de menu nos menus do Windows Explorer. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_MERGEMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968220"
---
# <a name="sfvm_mergemenu-message"></a><span data-ttu-id="fe30f-104">\_Mensagem SFVM MERGEMENU</span><span class="sxs-lookup"><span data-stu-id="fe30f-104">SFVM\_MERGEMENU message</span></span>

<span data-ttu-id="fe30f-105">Permite que o objeto de retorno de chamada mescle itens de menu nos menus do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="fe30f-105">Allows the callback object to merge menu items into the Windows Explorer menus.</span></span> <span data-ttu-id="fe30f-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="fe30f-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a><span data-ttu-id="fe30f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe30f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe30f-108">*pInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fe30f-108">*pInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe30f-109">Uma estrutura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contém as informações necessárias para mesclar os itens no menu.</span><span class="sxs-lookup"><span data-stu-id="fe30f-109">A [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information needed to merge the items into the menu.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe30f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe30f-110">Remarks</span></span>

<span data-ttu-id="fe30f-111">Essa mensagem serve essencialmente a mesma finalidade que [**IShellBrowser:: InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) e [**IShellBrowser:: SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) em uma exibição de pasta personalizada.</span><span class="sxs-lookup"><span data-stu-id="fe30f-111">This message serves essentially the same purpose as the [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) and [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in a custom folder view.</span></span> <span data-ttu-id="fe30f-112">Consulte a seção *usando o IShellBrowser para se comunicar com o Windows Explorer* de [implementando uma exibição de pasta](../lwef/nse-folderview.md) para uma discussão adicional.</span><span class="sxs-lookup"><span data-stu-id="fe30f-112">See the *Using IShellBrowser to Communicate with Windows Explorer* section of [Implementing a Folder View](../lwef/nse-folderview.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe30f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe30f-113">Requirements</span></span>



| <span data-ttu-id="fe30f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe30f-114">Requirement</span></span> | <span data-ttu-id="fe30f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fe30f-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe30f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe30f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe30f-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe30f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fe30f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe30f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe30f-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe30f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fe30f-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe30f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe30f-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe30f-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
