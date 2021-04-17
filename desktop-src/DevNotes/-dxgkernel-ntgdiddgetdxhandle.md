---
description: Retorna o identificador da API do Microsoft DirectX do modo kernel a ser usado em chamadas subsequentes para os pontos de entrada do modo kernel que controlam o mecanismo da API do DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Função NtGdiDdGetDxHandle (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752930"
---
# <a name="ntgdiddgetdxhandle-function"></a><span data-ttu-id="2d5ad-103">Função NtGdiDdGetDxHandle</span><span class="sxs-lookup"><span data-stu-id="2d5ad-103">NtGdiDdGetDxHandle function</span></span>

<span data-ttu-id="2d5ad-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="2d5ad-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="2d5ad-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="2d5ad-106">Retorna o identificador da API do Microsoft DirectX do modo kernel a ser usado em chamadas subsequentes para os pontos de entrada do modo kernel que controlam o mecanismo da API do DirectX.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-106">Returns the kernel-mode Microsoft DirectX  API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX  API mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d5ad-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d5ad-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a><span data-ttu-id="2d5ad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d5ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d5ad-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d5ad-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5ad-110">Identificador para o objeto do DirectDraw que possui a superfície.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-110">Handle to DirectDraw object owning the surface.</span></span> <span data-ttu-id="2d5ad-111">Esse parâmetro é opcional e pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-111">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2d5ad-112">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d5ad-112">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5ad-113">Identificador para superfície para o qual retornar um identificador de API DirectX do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-113">Handle to surface for which to return a kernel-mode DirectX API handle.</span></span> <span data-ttu-id="2d5ad-114">Esse parâmetro é opcional e pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-114">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2d5ad-115">*bRelease* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d5ad-115">*bRelease* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d5ad-116">Defina como **true** se a interface do modo kernel da API do DirectX for lançada.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-116">Set to **TRUE** if the DirectX API kernel mode interface should be released.</span></span> <span data-ttu-id="2d5ad-117">Caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-117">Otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d5ad-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d5ad-118">Return value</span></span>

<span data-ttu-id="2d5ad-119">Um identificador de API do DirectX usado em pontos de entrada do kernel com orientação de API do DirectX subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-119">A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d5ad-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d5ad-120">Remarks</span></span>

<span data-ttu-id="2d5ad-121">Se *hDirectDraw* e *hSurface* forem especificados, *hSurface* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="2d5ad-121">If both *hDirectDraw* and *hSurface* are specified, *hSurface* is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d5ad-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d5ad-122">Requirements</span></span>



| <span data-ttu-id="2d5ad-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d5ad-123">Requirement</span></span> | <span data-ttu-id="2d5ad-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2d5ad-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5ad-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d5ad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d5ad-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2d5ad-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2d5ad-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d5ad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d5ad-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2d5ad-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2d5ad-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2d5ad-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d5ad-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d5ad-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d5ad-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d5ad-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5ad-132">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="2d5ad-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




