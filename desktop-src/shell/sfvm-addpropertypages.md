---
description: 'Permite que o objeto de retorno de chamada forneça uma página a ser adicionada à folha de propriedades de propriedades do objeto selecionado. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_ADDPROPERTYPAGES (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989034"
---
# <a name="sfvm_addpropertypages-message"></a><span data-ttu-id="61c52-104">\_Mensagem SFVM ADDPROPERTYPAGES</span><span class="sxs-lookup"><span data-stu-id="61c52-104">SFVM\_ADDPROPERTYPAGES message</span></span>

<span data-ttu-id="61c52-105">Permite que o objeto de retorno de chamada forneça uma página a ser adicionada à folha de propriedades de **Propriedades** do objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="61c52-105">Allows the callback object to provide a page to add to the **Properties** property sheet of the selected object.</span></span> <span data-ttu-id="61c52-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="61c52-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a><span data-ttu-id="61c52-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61c52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61c52-108">*pData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="61c52-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61c52-109">O endereço de uma estrutura de [**\_ \_ dados SFVM PROPPAGE**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .</span><span class="sxs-lookup"><span data-stu-id="61c52-109">The address of a [**SFVM\_PROPPAGE\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61c52-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="61c52-110">Remarks</span></span>

<span data-ttu-id="61c52-111">Essa mensagem serve essencialmente a mesma função que [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="61c52-111">This message serves essentially the same function as [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span> <span data-ttu-id="61c52-112">Consulte [criando manipuladores de folha de propriedades](propsheet-handlers.md) para mais discussões.</span><span class="sxs-lookup"><span data-stu-id="61c52-112">See [Creating Property Sheet Handlers](propsheet-handlers.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="61c52-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61c52-113">Requirements</span></span>



| <span data-ttu-id="61c52-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61c52-114">Requirement</span></span> | <span data-ttu-id="61c52-115">Valor</span><span class="sxs-lookup"><span data-stu-id="61c52-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61c52-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61c52-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61c52-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61c52-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="61c52-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61c52-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61c52-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61c52-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="61c52-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61c52-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61c52-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="61c52-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
