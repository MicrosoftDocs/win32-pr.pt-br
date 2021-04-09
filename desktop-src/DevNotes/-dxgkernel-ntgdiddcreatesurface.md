---
description: Anexa uma superfície a outra superfície.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Função NtGdiDdCreateSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 663d29be32dc544d44a47061e1a6ff7f81e60862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088920"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="07c2a-103">Função NtGdiDdCreateSurface</span><span class="sxs-lookup"><span data-stu-id="07c2a-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="07c2a-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="07c2a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="07c2a-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="07c2a-106">Anexa uma superfície a outra superfície.</span><span class="sxs-lookup"><span data-stu-id="07c2a-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c2a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07c2a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="07c2a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07c2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c2a-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c2a-110">Manipule a estrutura [**\_ \_ global do DIRECTDRAW do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa o driver.</span><span class="sxs-lookup"><span data-stu-id="07c2a-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="07c2a-111">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c2a-112">Identificador anterior para a mesma superfície.</span><span class="sxs-lookup"><span data-stu-id="07c2a-112">Previous handle to the same surface.</span></span> <span data-ttu-id="07c2a-113">Usado se a superfície estiver sendo recriada após uma opção de modo.</span><span class="sxs-lookup"><span data-stu-id="07c2a-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="07c2a-114">*puSurfaceDescription* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c2a-115">Ponteiro para a estrutura [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que descreve a superfície ou o buffer que o driver deve criar.</span><span class="sxs-lookup"><span data-stu-id="07c2a-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="07c2a-116">*puSurfaceGlobalData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c2a-117">Ponteiro para a [**estrutura \_ \_ global da superfície DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contém dados de superfície que são compartilhados globalmente com várias superfícies.</span><span class="sxs-lookup"><span data-stu-id="07c2a-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="07c2a-118">*puSurfaceLocalData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c2a-119">Ponteiro para uma lista de [**estruturas \_ \_ locais de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descrevem os objetos de superfície criados pelo driver.</span><span class="sxs-lookup"><span data-stu-id="07c2a-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="07c2a-120">*puSurfaceMoreData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c2a-121">Ponteiro para uma [**superfície de DD \_ \_ mais**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estrutura que contém dados de superfície local adicionais.</span><span class="sxs-lookup"><span data-stu-id="07c2a-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="07c2a-122">*puCreateSurfaceData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c2a-123">Ponteiro para uma [**estrutura \_ CREATESURFACEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contém as informações necessárias para criar uma superfície.</span><span class="sxs-lookup"><span data-stu-id="07c2a-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="07c2a-124">*puhSurface* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07c2a-125">É usado pela API do DirectDraw e não deve ser preenchido pelo driver.</span><span class="sxs-lookup"><span data-stu-id="07c2a-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c2a-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07c2a-126">Return value</span></span>

<span data-ttu-id="07c2a-127">**NtGdiDdCreateSurface** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="07c2a-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="07c2a-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="07c2a-128">Return code</span></span>                                                                                              | <span data-ttu-id="07c2a-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="07c2a-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07c2a-130"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="07c2a-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="07c2a-131">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="07c2a-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="07c2a-132">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="07c2a-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="07c2a-133">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="07c2a-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="07c2a-134"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="07c2a-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="07c2a-135">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="07c2a-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="07c2a-136">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="07c2a-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="07c2a-137">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07c2a-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07c2a-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="07c2a-138">Remarks</span></span>

<span data-ttu-id="07c2a-139">É recomendável que seu aplicativo chame [IDirectDraw7:: CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) em vez de usar essa função.</span><span class="sxs-lookup"><span data-stu-id="07c2a-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="07c2a-140">Ao criar uma cadeia de superfícies anexadas, como uma cadeia de permuta ou cadeia ou mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) deve ser chamado para cada superfície primeiro.</span><span class="sxs-lookup"><span data-stu-id="07c2a-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="07c2a-141">Em seguida, chame [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) para anexá-los.</span><span class="sxs-lookup"><span data-stu-id="07c2a-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="07c2a-142">Por fim, chame **NtGdiDdCreateSurface** para a primeira superfície somente na cadeia.</span><span class="sxs-lookup"><span data-stu-id="07c2a-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="07c2a-143">Nesse caso, *hSurface* seria o identificador retornado por **NtGdiDdCreateSurfaceObject** para a primeira superfície na cadeia.</span><span class="sxs-lookup"><span data-stu-id="07c2a-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="07c2a-144">**NtGdiDdCreateSurface** só deve ser chamado para criar superfícies em memória de vídeo local e não local.</span><span class="sxs-lookup"><span data-stu-id="07c2a-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="07c2a-145">Ele nunca deve ser chamado para criar superfícies de memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="07c2a-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="07c2a-146">Para criar superfícies de memória do sistema, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="07c2a-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c2a-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c2a-147">Requirements</span></span>



| <span data-ttu-id="07c2a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c2a-148">Requirement</span></span> | <span data-ttu-id="07c2a-149">Valor</span><span class="sxs-lookup"><span data-stu-id="07c2a-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07c2a-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07c2a-150">Minimum supported client</span></span><br/> | <span data-ttu-id="07c2a-151">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="07c2a-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07c2a-152">Minimum supported server</span></span><br/> | <span data-ttu-id="07c2a-153">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="07c2a-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="07c2a-154">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="07c2a-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c2a-155"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="07c2a-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c2a-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="07c2a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c2a-157">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="07c2a-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
