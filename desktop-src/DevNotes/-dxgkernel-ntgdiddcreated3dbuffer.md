---
description: Usado para criar um comando no nível do driver ou um buffer de vértice da descrição especificada.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: Função NtGdiDdCreateD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920170"
---
# <a name="ntgdiddcreated3dbuffer-function"></a><span data-ttu-id="98629-103">Função NtGdiDdCreateD3DBuffer</span><span class="sxs-lookup"><span data-stu-id="98629-103">NtGdiDdCreateD3DBuffer function</span></span>

<span data-ttu-id="98629-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="98629-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="98629-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="98629-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="98629-106">Usado para criar um comando no nível do driver ou um buffer de vértice da descrição especificada.</span><span class="sxs-lookup"><span data-stu-id="98629-106">Used to create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="98629-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98629-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="98629-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98629-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98629-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98629-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98629-110">Manipule a estrutura [**\_ \_ global do DIRECTDRAW do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa o driver.</span><span class="sxs-lookup"><span data-stu-id="98629-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="98629-111">*hSurface* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98629-111">*hSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98629-112">Ponteiro para uma matriz de alças de superfície.</span><span class="sxs-lookup"><span data-stu-id="98629-112">Pointer to an array of surface handles.</span></span> <span data-ttu-id="98629-113">O chamador pode definir esses identificadores para os valores de identificador anteriores se as superfícies estiverem sendo recriadas após uma opção de modo.</span><span class="sxs-lookup"><span data-stu-id="98629-113">The caller can set these handles to the previous handle values if the surfaces are being re-created after a mode switch.</span></span> <span data-ttu-id="98629-114">Esse processo é chamado de "restauração" na documentação do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="98629-114">This process is called "restoring" in the DirectDraw documentation.</span></span>

</dd> <dt>

<span data-ttu-id="98629-115">*puSurfaceDescription* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98629-115">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98629-116">Ponteiro para uma estrutura [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que descreve a superfície ou o buffer que o driver deve criar.</span><span class="sxs-lookup"><span data-stu-id="98629-116">Pointer to a [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="98629-117">*puSurfaceGlobalData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98629-117">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98629-118">Ponteiro para uma [**estrutura \_ \_ global da superfície DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contém dados de superfície que são compartilhados globalmente com várias superfícies.</span><span class="sxs-lookup"><span data-stu-id="98629-118">Pointer to a [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="98629-119">*puSurfaceLocalData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98629-119">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98629-120">Ponteiro para uma lista de [**estruturas \_ \_ locais de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descrevem os objetos de superfície criados pelo driver.</span><span class="sxs-lookup"><span data-stu-id="98629-120">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span> <span data-ttu-id="98629-121">Normalmente, há apenas uma entrada nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="98629-121">There is usually only one entry in this array.</span></span>

</dd> <dt>

<span data-ttu-id="98629-122">*puSurfaceMoreData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98629-122">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98629-123">Ponteiro para uma [**superfície de DD \_ \_ mais**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estrutura que contém dados de superfície local adicionais.</span><span class="sxs-lookup"><span data-stu-id="98629-123">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="98629-124">*puCreateSurfaceData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98629-124">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98629-125">Ponteiro para uma [**estrutura \_ CREATESURFACEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contém as informações necessárias para criar o buffer.</span><span class="sxs-lookup"><span data-stu-id="98629-125">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="98629-126">*puhSurface* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="98629-126">*puhSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98629-127">É usado pela API do DirectDraw e não deve ser preenchido pelo driver.</span><span class="sxs-lookup"><span data-stu-id="98629-127">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98629-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98629-128">Return value</span></span>

<span data-ttu-id="98629-129">**NtGdiDdCreateD3DBuffer** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="98629-129">**NtGdiDdCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="98629-130">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="98629-130">Return code</span></span>                                                                                              | <span data-ttu-id="98629-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="98629-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98629-132"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="98629-132"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="98629-133">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="98629-133">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="98629-134">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="98629-134">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="98629-135">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="98629-135">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="98629-136"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="98629-136"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="98629-137">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="98629-137">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="98629-138">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="98629-138">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="98629-139">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98629-139">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98629-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98629-140">Requirements</span></span>



| <span data-ttu-id="98629-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="98629-141">Requirement</span></span> | <span data-ttu-id="98629-142">Valor</span><span class="sxs-lookup"><span data-stu-id="98629-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98629-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98629-143">Minimum supported client</span></span><br/> | <span data-ttu-id="98629-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="98629-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="98629-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98629-145">Minimum supported server</span></span><br/> | <span data-ttu-id="98629-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="98629-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="98629-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="98629-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="98629-148"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="98629-148"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98629-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="98629-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98629-150">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="98629-150">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
