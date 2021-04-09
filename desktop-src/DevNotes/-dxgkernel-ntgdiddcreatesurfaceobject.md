---
description: Cria um objeto de superfície do modo kernel que representa o objeto de superfície do modo de usuário referenciado por puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Função NtGdiDdCreateSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010111"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a><span data-ttu-id="0d19f-103">Função NtGdiDdCreateSurfaceObject</span><span class="sxs-lookup"><span data-stu-id="0d19f-103">NtGdiDdCreateSurfaceObject function</span></span>

<span data-ttu-id="0d19f-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0d19f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="0d19f-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="0d19f-106">Cria um objeto de superfície do modo kernel que representa o objeto de superfície do modo de usuário referenciado por *puSurfaceLocal*.</span><span class="sxs-lookup"><span data-stu-id="0d19f-106">Creates a kernel-mode surface object that represents the user-mode surface object referenced by *puSurfaceLocal*.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d19f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d19f-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a><span data-ttu-id="0d19f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d19f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d19f-109">*hDirectDrawLocal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d19f-110">Identificador para o objeto DirectDraw do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="0d19f-110">Handle to the kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="0d19f-111">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d19f-112">Identificador anterior para a mesma superfície.</span><span class="sxs-lookup"><span data-stu-id="0d19f-112">Previous handle to the same surface.</span></span> <span data-ttu-id="0d19f-113">Usado se a superfície estiver sendo recriada após uma opção de modo.</span><span class="sxs-lookup"><span data-stu-id="0d19f-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="0d19f-114">*puSurfaceLocal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-114">*puSurfaceLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d19f-115">Ponteiro para a [**estrutura \_ \_ local da superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa o objeto de superfície do modo de usuário do DirectDraw ao qual associar a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="0d19f-115">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw user-mode surface object with which to associate the allocated memory.</span></span> <span data-ttu-id="0d19f-116">Consulte a documentação do DDK para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="0d19f-116">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="0d19f-117">*puSurfaceMore* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-117">*puSurfaceMore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d19f-118">Aponta para a [**superfície de DD \_ \_ mais**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estrutura que contém dados locais adicionais para cada objeto de superfície individual.</span><span class="sxs-lookup"><span data-stu-id="0d19f-118">Pointer to the [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local data for each individual surface object.</span></span> <span data-ttu-id="0d19f-119">Consulte a documentação do DDK para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="0d19f-119">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="0d19f-120">*puSurfaceGlobal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-120">*puSurfaceGlobal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d19f-121">Ponteiro para a [**estrutura \_ \_ global da superfície DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contém dados de superfície compartilhados globalmente com várias superfícies.</span><span class="sxs-lookup"><span data-stu-id="0d19f-121">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure that contains surface data shared globally with multiple surfaces.</span></span> <span data-ttu-id="0d19f-122">Consulte a documentação do DDK para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="0d19f-122">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="0d19f-123">*bComplete* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-123">*bComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d19f-124">Sinalizador de conclusão de objeto em modo kernel.</span><span class="sxs-lookup"><span data-stu-id="0d19f-124">Kernel-mode object completion flag.</span></span> <span data-ttu-id="0d19f-125">Pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d19f-125">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="0d19f-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="0d19f-126">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="0d19f-127">Conclua todo o processamento em relação à representação do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="0d19f-127">Complete all processing concerning the kernel-mode representation.</span></span>

</dd> <dt>



 <span data-ttu-id="0d19f-128">FOR</span><span class="sxs-lookup"><span data-stu-id="0d19f-128">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="0d19f-129">Crie o objeto, mas não configure dados internos, como o ponteiro de memória.</span><span class="sxs-lookup"><span data-stu-id="0d19f-129">Create the object, but do not set up internal data such as the memory pointer.</span></span> <span data-ttu-id="0d19f-130">Os objetos criados usando **false** podem ser anexados usando [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) e são concluídos por uma chamada para [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span><span class="sxs-lookup"><span data-stu-id="0d19f-130">Objects created using **FALSE** can be attached using [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) and are completed by a call to [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d19f-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d19f-131">Return value</span></span>

<span data-ttu-id="0d19f-132">Se for bem-sucedida, essa função retornará um identificador para a representação de superfície do modo kernel; caso contrário, ele retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0d19f-132">If successful, this function returns a handle to the kernel-mode surface representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d19f-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d19f-133">Remarks</span></span>

<span data-ttu-id="0d19f-134">Os aplicativos são aconselhados a usar as APIs do DirectDraw e do [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="0d19f-134">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="0d19f-135">Essas construções abstraem o processo de criação de dispositivos de maneira simplificada e independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0d19f-135">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d19f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d19f-136">Requirements</span></span>



| <span data-ttu-id="0d19f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d19f-137">Requirement</span></span> | <span data-ttu-id="0d19f-138">Valor</span><span class="sxs-lookup"><span data-stu-id="0d19f-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d19f-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d19f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0d19f-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0d19f-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d19f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0d19f-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0d19f-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d19f-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0d19f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d19f-144"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d19f-144"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d19f-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d19f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d19f-146">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="0d19f-146">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="0d19f-147">**DdCreateSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="0d19f-147">**DdCreateSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[<span data-ttu-id="0d19f-148">**NtGdiDdDeleteSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="0d19f-148">**NtGdiDdDeleteSurfaceObject**</span></span>](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[<span data-ttu-id="0d19f-149">**NtGdiDdAttachSurface**</span><span class="sxs-lookup"><span data-stu-id="0d19f-149">**NtGdiDdAttachSurface**</span></span>](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[<span data-ttu-id="0d19f-150">**NtGdiDdCreateSurface**</span><span class="sxs-lookup"><span data-stu-id="0d19f-150">**NtGdiDdCreateSurface**</span></span>](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
