---
description: Cria um DC (contexto de dispositivo) para a superfície especificada.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Função NtGdiDdGetDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089189"
---
# <a name="ntgdiddgetdc-function"></a><span data-ttu-id="6c3c9-103">Função NtGdiDdGetDC</span><span class="sxs-lookup"><span data-stu-id="6c3c9-103">NtGdiDdGetDC function</span></span>

<span data-ttu-id="6c3c9-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6c3c9-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="6c3c9-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="6c3c9-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="6c3c9-106">Cria um DC (contexto de dispositivo) para a superfície especificada.</span><span class="sxs-lookup"><span data-stu-id="6c3c9-106">Creates a device context (DC) for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3c9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c3c9-107">Syntax</span></span>


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a><span data-ttu-id="6c3c9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c3c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3c9-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c3c9-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3c9-110">Identificador para uma superfície DirectDraw do modo kernel retornada anteriormente por [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) ou [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span><span class="sxs-lookup"><span data-stu-id="6c3c9-110">Handle to a kernel-mode DirectDraw surface previously returned by [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) or [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c3c9-111">*puColorTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c3c9-111">*puColorTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3c9-112">Ponteiro para uma tabela de cores de substituição para o DC retornado.</span><span class="sxs-lookup"><span data-stu-id="6c3c9-112">Pointer to an override color table for the returned DC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3c9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c3c9-113">Return value</span></span>

<span data-ttu-id="6c3c9-114">Se for bem-sucedida, essa função retornará um **HDC** válido; caso contrário, ele retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6c3c9-114">If successful, this function returns a valid **HDC**; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c3c9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c3c9-115">Remarks</span></span>

<span data-ttu-id="6c3c9-116">Somente um DC é permitido por superfície em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="6c3c9-116">Only one DC is allowed per surface at any given time.</span></span> <span data-ttu-id="6c3c9-117">As chamadas subsequentes para **NtGdiDdGetDC** falharão até que o controlador de domínio anterior seja liberado.</span><span class="sxs-lookup"><span data-stu-id="6c3c9-117">Subsequent calls to **NtGdiDdGetDC** will fail until the previous DC is released.</span></span>

<span data-ttu-id="6c3c9-118">Os aplicativos são aconselhados a chamar [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) em vez disso, que fornece a mesma funcionalidade de uma maneira independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6c3c9-118">Applications are advised to call [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) instead, which provides the same functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3c9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c3c9-119">Requirements</span></span>



| <span data-ttu-id="6c3c9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c3c9-120">Requirement</span></span> | <span data-ttu-id="6c3c9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6c3c9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3c9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c3c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3c9-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c3c9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6c3c9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c3c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3c9-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c3c9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c3c9-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c3c9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3c9-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3c9-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c3c9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c3c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3c9-129">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="6c3c9-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="6c3c9-130">**DdGetDC**</span><span class="sxs-lookup"><span data-stu-id="6c3c9-130">**DdGetDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
