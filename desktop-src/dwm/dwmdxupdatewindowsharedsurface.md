---
description: Notifica o DWM de uma atualização de entrada para uma superfície compartilhada da janela.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: Função DwmDxUpdateWindowSharedSurface
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502348"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a><span data-ttu-id="31f1b-103">Função DwmDxUpdateWindowSharedSurface</span><span class="sxs-lookup"><span data-stu-id="31f1b-103">DwmDxUpdateWindowSharedSurface function</span></span>

<span data-ttu-id="31f1b-104">Notifica o DWM de uma atualização de entrada para uma superfície compartilhada da janela.</span><span class="sxs-lookup"><span data-stu-id="31f1b-104">Notifies the DWM of an incoming update to a window shared surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f1b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31f1b-105">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a><span data-ttu-id="31f1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31f1b-106">Parameters</span></span>

`hwnd`

<span data-ttu-id="31f1b-107">Um [**HWND**](/windows/desktop/winprog/windows-data-types) que especifica a janela que está sendo atualizada.</span><span class="sxs-lookup"><span data-stu-id="31f1b-107">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window being updated.</span></span>

`uiUpdateId`

<span data-ttu-id="31f1b-108">A ID de atualização recuperada de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span><span class="sxs-lookup"><span data-stu-id="31f1b-108">The update ID retrieved from [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).</span></span>

`dwFlags`

<span data-ttu-id="31f1b-109">Reservado.</span><span class="sxs-lookup"><span data-stu-id="31f1b-109">Reserved.</span></span>

`hmonitorAssociation`

<span data-ttu-id="31f1b-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="31f1b-110">Reserved.</span></span>

`prc`

<span data-ttu-id="31f1b-111">O Rect da janela que está sendo atualizada, no espaço de coordenadas da janela.</span><span class="sxs-lookup"><span data-stu-id="31f1b-111">The rect of the window being updated, in window coordinate space.</span></span> <span data-ttu-id="31f1b-112">Um retângulo nulo indica que nenhuma região foi atualizada.</span><span class="sxs-lookup"><span data-stu-id="31f1b-112">A NULL rectangle indicates that no region was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="31f1b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31f1b-113">Return value</span></span>

<span data-ttu-id="31f1b-114">**S \_ OK** se for bem-sucedido, caso contrário, um HRESULT com falha **.**</span><span class="sxs-lookup"><span data-stu-id="31f1b-114">**S\_OK** if successful, otherwise a FAILED **HRESULT.**</span></span>

## <a name="remarks"></a><span data-ttu-id="31f1b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="31f1b-115">Remarks</span></span>

<span data-ttu-id="31f1b-116">Essa API destina-se à implementação de um driver de gráficos ou tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="31f1b-116">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="31f1b-117">Um aplicativo pode não chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="31f1b-117">An application may not call this method.</span></span> <span data-ttu-id="31f1b-118">Esta documentação só é válida para o Windows 7, e não há garantia de que essa API exista nem se comporte de maneira semelhante em outras versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="31f1b-118">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="31f1b-119">Essa função não está presente em nenhum cabeçalho ou biblioteca de vínculo estático, e está localizada no ordinal 101 em dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="31f1b-119">This function is not present in any header or static-link library, and it is located at ordinal 101 in dwmapi.dll.</span></span>

<span data-ttu-id="31f1b-120">Esse método só deve ser chamado depois de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) retornar **S \_ OK** e deve ser chamado nesse cenário, independentemente de a superfície ser atualizada ou não.</span><span class="sxs-lookup"><span data-stu-id="31f1b-120">This method should only ever be called after [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) returns **S\_OK**, and must be called in that scenario, regardless of whether the surface is updated or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="31f1b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f1b-121">Requirements</span></span>

| <span data-ttu-id="31f1b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f1b-122">Requirement</span></span> | <span data-ttu-id="31f1b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="31f1b-123">Value</span></span> |
|-|-|
| <span data-ttu-id="31f1b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31f1b-124">Minimum supported client</span></span> | <span data-ttu-id="31f1b-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="31f1b-125">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="31f1b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31f1b-126">Minimum supported server</span></span> | <span data-ttu-id="31f1b-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="31f1b-127">None supported</span></span> |
| <span data-ttu-id="31f1b-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="31f1b-128">End of client support</span></span> | <span data-ttu-id="31f1b-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31f1b-129">Windows 7</span></span> |
| <span data-ttu-id="31f1b-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31f1b-130">Header</span></span> | <span data-ttu-id="31f1b-131">N/D</span><span class="sxs-lookup"><span data-stu-id="31f1b-131">N/A</span></span> |
| <span data-ttu-id="31f1b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="31f1b-132">DLL</span></span> | <span data-ttu-id="31f1b-133">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="31f1b-133">Dwmapi.dll</span></span> |
