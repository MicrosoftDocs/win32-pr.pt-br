---
title: HWINEVENTHOOK (windef. h)
description: Usado para declarar uma função de gancho de evento de janela.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763886"
---
# <a name="hwineventhook"></a><span data-ttu-id="848ff-104">HWINEVENTHOOK</span><span class="sxs-lookup"><span data-stu-id="848ff-104">HWINEVENTHOOK</span></span>

<span data-ttu-id="848ff-105">Usado para declarar uma função de gancho de evento de janela.</span><span class="sxs-lookup"><span data-stu-id="848ff-105">Used to declare a window event hook function.</span></span>


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a><span data-ttu-id="848ff-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="848ff-106">Remarks</span></span>

<span data-ttu-id="848ff-107">Esse tipo de dados é usado com a função de retorno de chamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e as funções [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .</span><span class="sxs-lookup"><span data-stu-id="848ff-107">This data type is used with the [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function and the [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="848ff-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="848ff-108">Requirements</span></span>



| <span data-ttu-id="848ff-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="848ff-109">Requirement</span></span> | <span data-ttu-id="848ff-110">Valor</span><span class="sxs-lookup"><span data-stu-id="848ff-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="848ff-111">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="848ff-111">Minimum supported client</span></span><br/> | <span data-ttu-id="848ff-112">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="848ff-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="848ff-113">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="848ff-113">Minimum supported server</span></span><br/> | <span data-ttu-id="848ff-114">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="848ff-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                          |
| <span data-ttu-id="848ff-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="848ff-115">Redistributable</span></span><br/>          | <span data-ttu-id="848ff-116">Acessibilidade Ativa 1,3 RDK no Windows NT 4,0 com SP6 e posterior e Windows 95</span><span class="sxs-lookup"><span data-stu-id="848ff-116">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>                                   |
| <span data-ttu-id="848ff-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="848ff-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="848ff-118"><dt>Windef. h (WINVER >= 0x0500) (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="848ff-118"><dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt></span></span> </dl> |



 

 





