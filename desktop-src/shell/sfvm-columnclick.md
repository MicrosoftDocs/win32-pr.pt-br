---
description: 'Notifica o objeto de retorno de chamada que o usuário clicou em um cabeçalho de coluna para classificar a lista de objetos no modo de exibição de pasta. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_COLUMNCLICK (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461258"
---
# <a name="sfvm_columnclick-message"></a><span data-ttu-id="bc257-104">\_Mensagem SFVM COLUMNCLICK</span><span class="sxs-lookup"><span data-stu-id="bc257-104">SFVM\_COLUMNCLICK message</span></span>

<span data-ttu-id="bc257-105">Notifica o objeto de retorno de chamada que o usuário clicou em um cabeçalho de coluna para classificar a lista de objetos no modo de exibição de pasta.</span><span class="sxs-lookup"><span data-stu-id="bc257-105">Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</span></span> <span data-ttu-id="bc257-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="bc257-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="bc257-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc257-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc257-108">*IColumn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc257-108">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc257-109">O índice da coluna que foi clicada.</span><span class="sxs-lookup"><span data-stu-id="bc257-109">The index of the column that was clicked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc257-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc257-110">Remarks</span></span>

<span data-ttu-id="bc257-111">Em resposta a essa notificação, você deve retornar S \_ OK para reorganizar a lista por conta própria.</span><span class="sxs-lookup"><span data-stu-id="bc257-111">In response to this notification, you should return S\_OK to rearrange the list yourself.</span></span> <span data-ttu-id="bc257-112">Para que a pasta do sistema exiba o objeto, reorganize a lista, retorne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="bc257-112">To have the system folder view object rearrange the list, return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc257-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc257-113">Requirements</span></span>



| <span data-ttu-id="bc257-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc257-114">Requirement</span></span> | <span data-ttu-id="bc257-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bc257-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bc257-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc257-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc257-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc257-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bc257-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc257-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc257-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bc257-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bc257-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bc257-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc257-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc257-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
