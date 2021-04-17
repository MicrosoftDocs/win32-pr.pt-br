---
description: Recupera a superfície compartilhada do DirectX fazendo backup de uma determinada janela. Essa superfície pode ser gravada para atualizar o conteúdo da janela.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: Função DwmDxGetWindowSharedSurface
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
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766415"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a><span data-ttu-id="83807-104">Função DwmDxGetWindowSharedSurface</span><span class="sxs-lookup"><span data-stu-id="83807-104">DwmDxGetWindowSharedSurface function</span></span>

<span data-ttu-id="83807-105">Recupera a superfície compartilhada do DirectX fazendo backup de uma determinada janela.</span><span class="sxs-lookup"><span data-stu-id="83807-105">Retrieves the DirectX shared surface backing a given window.</span></span> <span data-ttu-id="83807-106">Essa superfície pode ser gravada para atualizar o conteúdo da janela.</span><span class="sxs-lookup"><span data-stu-id="83807-106">This surface can be written to in order to update the contents of the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="83807-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83807-107">Syntax</span></span>

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a><span data-ttu-id="83807-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83807-108">Parameters</span></span>

`hwnd`

<span data-ttu-id="83807-109">Um [**HWND**](/windows/desktop/winprog/windows-data-types) que especifica a janela a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="83807-109">An [**HWND**](/windows/desktop/winprog/windows-data-types) specifying the window to be updated.</span></span>

`luidAdapter`

<span data-ttu-id="83807-110">O [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) do adaptador em que a superfície deve ser localizada.</span><span class="sxs-lookup"><span data-stu-id="83807-110">The [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) of the adapter where the surface should be located.</span></span>

`hmonitorAssociation`

<span data-ttu-id="83807-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="83807-111">Reserved.</span></span>

`dwFlags`

<span data-ttu-id="83807-112">Esse parâmetro pode ser um dos valores a seguir, ou uma combinação de bits ou de vários valores, quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="83807-112">This parameter can be one of the following values, or a bitwise OR combination of multiple values where appropriate.</span></span>

| <span data-ttu-id="83807-113">Valor</span><span class="sxs-lookup"><span data-stu-id="83807-113">Value</span></span> | <span data-ttu-id="83807-114">Significado</span><span class="sxs-lookup"><span data-stu-id="83807-114">Meaning</span></span> |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <span data-ttu-id="83807-115"><dt>**DWM \_ Sinalizador de redirecionamento de \_ \_ espera**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83807-115"><dt>**DWM\_REDIRECTION\_FLAG\_WAIT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="83807-116">Faz com que a função seja bloqueada até que uma sincronização vertical (VSync) tenha passado desde a última vez que a função foi chamada com êxito.</span><span class="sxs-lookup"><span data-stu-id="83807-116">Causes the function to block until a vertical synchronization (VSync) has passed since the last time the function was called successfully.</span></span> |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <span data-ttu-id="83807-117"><dt>**DWM \_ Suporte ao sinalizador de redirecionamento \_ \_ \_ presente \_ na \_ \_ superfície do GDI**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="83807-117"><dt>**DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="83807-118">Indica que o aplicativo de chamada é capaz de apresentar a uma superfície compartilhada GDI.</span><span class="sxs-lookup"><span data-stu-id="83807-118">Indicates that the calling application is capable of presenting to a GDI shared surface.</span></span> |

`pfmtWindow`

<span data-ttu-id="83807-119">Na entrada, o formato desejado da superfície.</span><span class="sxs-lookup"><span data-stu-id="83807-119">On input, the desired format of the surface.</span></span> <span data-ttu-id="83807-120">Na saída, o formato real da superfície retornada.</span><span class="sxs-lookup"><span data-stu-id="83807-120">On output, the actual format of the returned surface.</span></span>

`phDxSurface`

<span data-ttu-id="83807-121">Na saída, o identificador compartilhado para a superfície.</span><span class="sxs-lookup"><span data-stu-id="83807-121">On output, the shared handle to the surface.</span></span>

`puiUpdateId`

<span data-ttu-id="83807-122">Na saída, a ID da atualização.</span><span class="sxs-lookup"><span data-stu-id="83807-122">On output, the ID of the update.</span></span>

## <a name="return-value"></a><span data-ttu-id="83807-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83807-123">Return value</span></span>

<span data-ttu-id="83807-124">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="83807-124">This function can return one of these values.</span></span>

| <span data-ttu-id="83807-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="83807-125">Return code</span></span> | <span data-ttu-id="83807-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="83807-126">Description</span></span> |
|-|-|
| <span data-ttu-id="83807-127">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="83807-127">**S\_OK**</span></span> | <span data-ttu-id="83807-128">A chamada foi bem-sucedida, e você deve atualizar a superfície, passando a ID de atualização para [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (no membro **PresentHistoryToken** da estrutura de **\_ renderização D3DKMT** quando a atualização é enviada e, em seguida, [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) deve ser chamado com a mesma ID de atualização.</span><span class="sxs-lookup"><span data-stu-id="83807-128">The call succeeded, and you should update the surface, being sure to pass the update ID to [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (in the **PresentHistoryToken** member of the **D3DKMT\_RENDER** structure when the update is submitted, and then [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) should be called with the same update ID.</span></span> <span data-ttu-id="83807-129">Observe que **DwmDxUpdateWindowSharedSurface** deve ser chamado independentemente de a superfície ter sido realmente atualizada ou não.</span><span class="sxs-lookup"><span data-stu-id="83807-129">Note that **DwmDxUpdateWindowSharedSurface** should be called regardless of whether the surface was actually updated or not.</span></span> |
| <span data-ttu-id="83807-130">**\_superfície de \_ \_ redirecionamento GDI do DWM S \_**</span><span class="sxs-lookup"><span data-stu-id="83807-130">**DWM\_S\_GDI\_REDIRECTION\_SURFACE**</span></span> | <span data-ttu-id="83807-131">A chamada foi bem-sucedida e você deve atualizar a superfície chamando [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)e definindo o **modelo** do membro **PRESENTHISTORYTOKEN** como **D3DKMT \_ PM \_ Redirecionado \_ BLT** e fornecendo a ID de atualização no membro **BLT** da União.</span><span class="sxs-lookup"><span data-stu-id="83807-131">The call succeeded, and you should update the surface by calling [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent), and setting **PresentHistoryToken** member's **Model** to **D3DKMT\_PM\_REDIRECTED\_BLT**, and providing the update ID in the **Blt** member of the union.</span></span> <span data-ttu-id="83807-132">Esse valor só será retornado se **o \_ suporte a sinalizador de redirecionamento \_ \_ de DWM \_ presente \_ para a \_ \_ superfície GDI** tiver sido especificado em *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="83807-132">This value is only returned if **DWM\_REDIRECTION\_FLAG\_SUPPORT\_PRESENT\_TO\_GDI\_SURFACE** was specified in *dwFlags*.</span></span> |
| <span data-ttu-id="83807-133">**DWM \_ E \_ adaptador \_ não \_ encontrados**</span><span class="sxs-lookup"><span data-stu-id="83807-133">**DWM\_E\_ADAPTER\_NOT\_FOUND**</span></span> | <span data-ttu-id="83807-134">O valor de *luidAdapter* não é válido.</span><span class="sxs-lookup"><span data-stu-id="83807-134">The value of *luidAdapter* is not valid.</span></span> |
| <span data-ttu-id="83807-135">**DWM \_ E \_ COMPOSITIONDISABLED**</span><span class="sxs-lookup"><span data-stu-id="83807-135">**DWM\_E\_COMPOSITIONDISABLED**</span></span> | <span data-ttu-id="83807-136">O DWM não está habilitado no momento e o aplicativo precisará apresentar outra maneira.</span><span class="sxs-lookup"><span data-stu-id="83807-136">DWM is not currently enabled, and the application will need to present another way.</span></span> |

## <a name="remarks"></a><span data-ttu-id="83807-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="83807-137">Remarks</span></span>

<span data-ttu-id="83807-138">Essa API destina-se à implementação de um driver de gráficos ou tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="83807-138">This API is intended for implementing a graphics driver or runtime.</span></span> <span data-ttu-id="83807-139">Um aplicativo pode não chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="83807-139">An application may not call this method.</span></span> <span data-ttu-id="83807-140">Esta documentação só é válida para o Windows 7, e não há garantia de que essa API exista nem se comporte de maneira semelhante em outras versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="83807-140">This documentation is only valid for Windows 7, and this API is not guaranteed to exist nor behave in a similar manner on other versions of Windows.</span></span> <span data-ttu-id="83807-141">Essa função não está presente em nenhum cabeçalho ou biblioteca de vínculo estático, e está localizada no ordinal 100 em dwmapi.dll.</span><span class="sxs-lookup"><span data-stu-id="83807-141">This function is not present in any header or static-link library, and it is located at ordinal 100 in dwmapi.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="83807-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83807-142">Requirements</span></span>

| <span data-ttu-id="83807-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="83807-143">Requirement</span></span> | <span data-ttu-id="83807-144">Valor</span><span class="sxs-lookup"><span data-stu-id="83807-144">Value</span></span> |
|-|-|
| <span data-ttu-id="83807-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83807-145">Minimum supported client</span></span> | <span data-ttu-id="83807-146">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="83807-146">Windows 7 \[desktop apps only\]</span></span> |
| <span data-ttu-id="83807-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83807-147">Minimum supported server</span></span> | <span data-ttu-id="83807-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="83807-148">None supported</span></span> |
| <span data-ttu-id="83807-149">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="83807-149">End of client support</span></span> | <span data-ttu-id="83807-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83807-150">Windows 7</span></span> |
| <span data-ttu-id="83807-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="83807-151">Header</span></span> | <span data-ttu-id="83807-152">N/D</span><span class="sxs-lookup"><span data-stu-id="83807-152">N/A</span></span> |
| <span data-ttu-id="83807-153">DLL</span><span class="sxs-lookup"><span data-stu-id="83807-153">DLL</span></span> | <span data-ttu-id="83807-154">Dwmapi.dll</span><span class="sxs-lookup"><span data-stu-id="83807-154">Dwmapi.dll</span></span> |
