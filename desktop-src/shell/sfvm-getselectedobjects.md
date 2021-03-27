---
description: Recupera uma matriz de ponteiros para listas de identificadores de item (PIDLs) para todos os objetos selecionados. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_GETSELECTEDOBJECTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837228"
---
# <a name="sfvm_getselectedobjects-message"></a><span data-ttu-id="bf4dc-104">\_Mensagem SFVM GETSELECTEDOBJECTS</span><span class="sxs-lookup"><span data-stu-id="bf4dc-104">SFVM\_GETSELECTEDOBJECTS message</span></span>

<span data-ttu-id="bf4dc-105">Recupera uma matriz de ponteiros para listas de identificadores de item (PIDLs) para todos os objetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-105">Retrieves an array of pointers to item identifier lists (PIDLs) for all selected objects.</span></span> <span data-ttu-id="bf4dc-106">Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="bf4dc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf4dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf4dc-108">*ppidl* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bf4dc-108">*ppidl* \[out\]</span></span>
</dt> <dd><span data-ttu-id="bf4dc-109">O endereço de uma matriz de PIDLs dos objetos selecionados no momento.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-109">The address of an array of PIDLs of currently selected objects.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf4dc-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf4dc-110">Return value</span></span>

<span data-ttu-id="bf4dc-111">Retorna o número de itens na matriz.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-111">Returns the number of items in the array.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf4dc-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf4dc-112">Remarks</span></span>

<span data-ttu-id="bf4dc-113">Quando terminar, você deve chamar [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) em cada membro da matriz para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-113">When finished, you should call [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) on each member of the array to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf4dc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf4dc-114">Requirements</span></span>



| <span data-ttu-id="bf4dc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf4dc-115">Requirement</span></span> | <span data-ttu-id="bf4dc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bf4dc-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bf4dc-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf4dc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf4dc-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bf4dc-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bf4dc-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf4dc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf4dc-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bf4dc-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bf4dc-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bf4dc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf4dc-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf4dc-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




