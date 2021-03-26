---
UID: ''
title: Função SHIsChildOrSelf
description: Compara se uma janela é igual a, um filho de ou um descendente de uma segunda janela.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104988639"
---
# <a name="shischildorself-function"></a><span data-ttu-id="c2a29-103">Função SHIsChildOrSelf</span><span class="sxs-lookup"><span data-stu-id="c2a29-103">SHIsChildOrSelf function</span></span>

## <a name="description"></a><span data-ttu-id="c2a29-104">Description</span><span class="sxs-lookup"><span data-stu-id="c2a29-104">Description</span></span>

<span data-ttu-id="c2a29-105">\[Essa função está disponível por meio do Windows XP e do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c2a29-105">\[This function is available through Windows XP and Windows Server 2003.</span></span>
<span data-ttu-id="c2a29-106">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2a29-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c2a29-107">Compara se uma janela é igual a, um filho de ou um descendente de uma segunda janela.</span><span class="sxs-lookup"><span data-stu-id="c2a29-107">Compares whether a window is equal to, a child of, or a descendant of, a second window.</span></span>

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a><span data-ttu-id="c2a29-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2a29-108">Parameters</span></span>

### <a name="hwndparent-in"></a><span data-ttu-id="c2a29-109">hwndParent [in]</span><span class="sxs-lookup"><span data-stu-id="c2a29-109">hwndParent [in]</span></span>

<span data-ttu-id="c2a29-110">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="c2a29-110">Type: **HWND**</span></span>

<span data-ttu-id="c2a29-111">Um identificador para a primeira janela.</span><span class="sxs-lookup"><span data-stu-id="c2a29-111">A handle to the first window.</span></span>

### <a name="hwnd-in"></a><span data-ttu-id="c2a29-112">HWND [in]</span><span class="sxs-lookup"><span data-stu-id="c2a29-112">hwnd [in]</span></span>

<span data-ttu-id="c2a29-113">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="c2a29-113">Type: **HWND**</span></span>

<span data-ttu-id="c2a29-114">Um identificador para uma janela a ser testado em relação a *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="c2a29-114">A handle to a window to be tested against *hwndParent*.</span></span>

## <a name="returns"></a><span data-ttu-id="c2a29-115">Retornos</span><span class="sxs-lookup"><span data-stu-id="c2a29-115">Returns</span></span>

<span data-ttu-id="c2a29-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c2a29-116">Type: **HRESULT**</span></span>

<span data-ttu-id="c2a29-117">Retorna **S_OK** se a janela especificada por *HWND* é igual a, um filho de ou um descendente da janela especificada por *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="c2a29-117">Returns **S_OK** if the window specified by *hwnd* is equal to, a child of, or a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="c2a29-118">Retorna **S_FALSE** se a janela especificada por HWND não for igual a, não um filho de, e não um descendente da janela especificada por *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="c2a29-118">Returns **S_FALSE** if the window specified by hwnd is not equal to, not a child of, and not a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="c2a29-119">O valor de retorno será indefinido se o identificador da janela for inválido.</span><span class="sxs-lookup"><span data-stu-id="c2a29-119">The return value is undefined if either window handle is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2a29-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2a29-120">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="c2a29-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2a29-121">See also</span></span>

[<span data-ttu-id="c2a29-122">IsChild</span><span class="sxs-lookup"><span data-stu-id="c2a29-122">IsChild</span></span>](/windows/desktop/api/winuser/nf-winuser-ischild)
