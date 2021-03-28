---
description: 'Permite que o objeto de retorno de chamada especifique que uma animação seja exibida enquanto os itens são enumerados em um thread em segundo plano. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Mensagem de SFVM_GETANIMATION (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091771"
---
# <a name="sfvm_getanimation-message"></a><span data-ttu-id="e4a93-104">\_Mensagem GETanimation do SFVM</span><span class="sxs-lookup"><span data-stu-id="e4a93-104">SFVM\_GETANIMATION message</span></span>

<span data-ttu-id="e4a93-105">Permite que o objeto de retorno de chamada especifique que uma animação seja exibida enquanto os itens são enumerados em um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e4a93-105">Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</span></span> <span data-ttu-id="e4a93-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="e4a93-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a><span data-ttu-id="e4a93-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4a93-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4a93-108">*phinst* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e4a93-108">*phinst* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a93-109">O identificador de instância do módulo do qual o recurso deve ser carregado.</span><span class="sxs-lookup"><span data-stu-id="e4a93-109">The instance handle of the module that the resource should be loaded from.</span></span>

</dd> <dt>

<span data-ttu-id="e4a93-110">*pwszName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e4a93-110">*pwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a93-111">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o caminho do arquivo. avi ou o nome de um recurso AVI.</span><span class="sxs-lookup"><span data-stu-id="e4a93-111">A pointer to a null-terminated Unicode string containing the path of the .avi file or the name of an AVI resource.</span></span> <span data-ttu-id="e4a93-112">Como alternativa, esse parâmetro pode consistir no identificador de recurso na palavra de ordem inferior e 0 na palavra de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="e4a93-112">Alternatively, this parameter can consist of the resource identifier in the low-order word and 0 in the high-order word.</span></span> <span data-ttu-id="e4a93-113">Para criar esse valor, use a macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="e4a93-113">To create this value, use the [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="e4a93-114">O controle carrega o recurso do módulo especificado por hinst.</span><span class="sxs-lookup"><span data-stu-id="e4a93-114">The control loads the resource from the module specified by hinst.</span></span> <span data-ttu-id="e4a93-115">Um recurso AVI deve ter o tipo "AVI".</span><span class="sxs-lookup"><span data-stu-id="e4a93-115">An AVI resource must have the "AVI" type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4a93-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4a93-116">Remarks</span></span>

<span data-ttu-id="e4a93-117">Por padrão, o objeto de exibição de pasta do sistema exibe a animação "lanterna" durante uma enumeração em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e4a93-117">By default, the system folder view object displays the "flashlight" animation during a background enumeration.</span></span>

<span data-ttu-id="e4a93-118">*phinst* e *pwszName* serão passados para o [controle de animação](../controls/animation-control-overview.md) com uma [**mensagem \_ aberta do ACM**](../controls/acm-open.md) .</span><span class="sxs-lookup"><span data-stu-id="e4a93-118">*phinst* and *pwszName* will be passed to the [animation control](../controls/animation-control-overview.md) with an [**ACM\_OPEN**](../controls/acm-open.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a93-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4a93-119">Requirements</span></span>



| <span data-ttu-id="e4a93-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4a93-120">Requirement</span></span> | <span data-ttu-id="e4a93-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e4a93-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a93-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a93-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a93-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4a93-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e4a93-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a93-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a93-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4a93-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e4a93-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e4a93-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4a93-127"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4a93-127"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
