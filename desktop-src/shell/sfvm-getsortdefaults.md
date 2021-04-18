---
description: 'Permite que o objeto de retorno de chamada especifique um parâmetro de classificação padrão. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_GETSORTDEFAULTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968233"
---
# <a name="sfvm_getsortdefaults-message"></a><span data-ttu-id="f4abe-104">\_Mensagem SFVM GETSORTDEFAULTS</span><span class="sxs-lookup"><span data-stu-id="f4abe-104">SFVM\_GETSORTDEFAULTS message</span></span>

<span data-ttu-id="f4abe-105">Permite que o objeto de retorno de chamada especifique um parâmetro de classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="f4abe-105">Allows the callback object to specify a default sorting parameter.</span></span> <span data-ttu-id="f4abe-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="f4abe-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="f4abe-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4abe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4abe-108">*iDirection* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f4abe-108">*iDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4abe-109">A direção de classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="f4abe-109">The default sorting direction.</span></span> <span data-ttu-id="f4abe-110">Defina esse parâmetro como um valor positivo para classificar em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="f4abe-110">Set this parameter to a positive value to sort in ascending order.</span></span> <span data-ttu-id="f4abe-111">Defina esse parâmetro como zero ou um valor negativo para classificar em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="f4abe-111">Set this parameter to zero or a negative value to sort in descending order.</span></span>

</dd> <dt>

<span data-ttu-id="f4abe-112">*IColumn* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f4abe-112">*iColumn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4abe-113">A coluna usada para a classificação.</span><span class="sxs-lookup"><span data-stu-id="f4abe-113">The column used for the sort.</span></span> <span data-ttu-id="f4abe-114">Isso será passado para o [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) nos menores 16 bits do seu valor de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f4abe-114">This will be passed to the [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in the lower 16 bits of its *lParam* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4abe-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4abe-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4abe-116">: **SFVM \_ GETSORTDEFAULTS** não é reconhecido pelo objeto de exibição de pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="f4abe-116">: **SFVM\_GETSORTDEFAULTS** is not recognized by the system folder view object.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4abe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4abe-117">Requirements</span></span>



| <span data-ttu-id="f4abe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4abe-118">Requirement</span></span> | <span data-ttu-id="f4abe-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f4abe-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f4abe-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4abe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4abe-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4abe-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f4abe-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4abe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4abe-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4abe-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f4abe-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f4abe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4abe-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4abe-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
