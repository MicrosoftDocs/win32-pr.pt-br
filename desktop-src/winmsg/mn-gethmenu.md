---
description: Recupera o identificador de menu para a janela atual.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Mensagem de MN_GETHMENU (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169567"
---
# <a name="mn_gethmenu-message"></a><span data-ttu-id="1ee7f-103">\_Mensagem GETHMENU MN</span><span class="sxs-lookup"><span data-stu-id="1ee7f-103">MN\_GETHMENU message</span></span>

<span data-ttu-id="1ee7f-104">Recupera o identificador de menu para a janela atual.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-104">Retrieves the menu handle for the current window.</span></span>


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a><span data-ttu-id="1ee7f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ee7f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee7f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ee7f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee7f-107">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1ee7f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ee7f-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee7f-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee7f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ee7f-110">Return value</span></span>

<span data-ttu-id="1ee7f-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="1ee7f-111">Type: **HMENU**</span></span>

<span data-ttu-id="1ee7f-112">Se for bem-sucedido, o valor de retorno será o **HMENU** para a janela atual.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-112">If successful, the return value is the **HMENU** for the current window.</span></span> <span data-ttu-id="1ee7f-113">Se falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1ee7f-113">If it fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee7f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ee7f-114">Requirements</span></span>



| <span data-ttu-id="1ee7f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee7f-115">Requirement</span></span> | <span data-ttu-id="1ee7f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1ee7f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee7f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ee7f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee7f-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ee7f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1ee7f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ee7f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee7f-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ee7f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ee7f-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ee7f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee7f-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee7f-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 




