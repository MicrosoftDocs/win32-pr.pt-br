---
description: Enviado pela implementação do menu de contexto padrão para atribuir um nome a um comando de menu.
title: Mensagem de DFM_MAPCOMMANDNAME (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501424"
---
# <a name="dfm_mapcommandname-message"></a><span data-ttu-id="43c3f-103">\_Mensagem DFM MAPCOMMANDNAME</span><span class="sxs-lookup"><span data-stu-id="43c3f-103">DFM\_MAPCOMMANDNAME message</span></span>

<span data-ttu-id="43c3f-104">Enviado pela implementação do menu de contexto padrão para atribuir um nome a um comando de menu.</span><span class="sxs-lookup"><span data-stu-id="43c3f-104">Sent by the default context menu implementation to assign a name to a menu command.</span></span>


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a><span data-ttu-id="43c3f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43c3f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c3f-106">*definição de padrão* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="43c3f-106">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43c3f-107">Um ponteiro para a ID do comando de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="43c3f-107">A pointer to the ID of the selected menu command.</span></span>

</dd> <dt>

<span data-ttu-id="43c3f-108">*pszCommandName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43c3f-108">*pszCommandName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43c3f-109">Um ponteiro para uma cadeia de caracteres Unicode que contém o nome do comando.</span><span class="sxs-lookup"><span data-stu-id="43c3f-109">A pointer to a Unicode string containing the name of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43c3f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="43c3f-110">Remarks</span></span>

<span data-ttu-id="43c3f-111">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é implementado.</span><span class="sxs-lookup"><span data-stu-id="43c3f-111">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="43c3f-112">Há duas APIs para sua implementação, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="43c3f-112">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="43c3f-113">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="43c3f-113">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="43c3f-114">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="43c3f-114">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c3f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43c3f-115">Requirements</span></span>



| <span data-ttu-id="43c3f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="43c3f-116">Requirement</span></span> | <span data-ttu-id="43c3f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="43c3f-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="43c3f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43c3f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="43c3f-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43c3f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="43c3f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43c3f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="43c3f-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43c3f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="43c3f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43c3f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="43c3f-123"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="43c3f-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




