---
description: Anexa duas representações de superfície no modo kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Função NtGdiDdAttachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755816"
---
# <a name="ntgdiddattachsurface-function"></a><span data-ttu-id="d8265-103">Função NtGdiDdAttachSurface</span><span class="sxs-lookup"><span data-stu-id="d8265-103">NtGdiDdAttachSurface function</span></span>

<span data-ttu-id="d8265-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d8265-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d8265-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="d8265-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d8265-106">Anexa duas representações de superfície no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="d8265-106">Attaches two kernel-mode surface representations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8265-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8265-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a><span data-ttu-id="d8265-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8265-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8265-109">*hSurfaceFrom* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8265-109">*hSurfaceFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8265-110">Identificador do objeto de superfície do modo kernel que será o ponto inicial do novo anexo.</span><span class="sxs-lookup"><span data-stu-id="d8265-110">Handle to kernel-mode surface object that will be the start point of the new attachment.</span></span>

</dd> <dt>

<span data-ttu-id="d8265-111">*hSurfaceTo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8265-111">*hSurfaceTo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8265-112">Identificador do objeto de superfície do modo kernel que será o ponto final do novo anexo.</span><span class="sxs-lookup"><span data-stu-id="d8265-112">Handle to kernel-mode surface object that will be the end point of the new attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8265-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8265-113">Return value</span></span>

<span data-ttu-id="d8265-114">**NtGdiDdAttachSurface** retorna um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d8265-114">**NtGdiDdAttachSurface** returns one of the following:</span></span>



| <span data-ttu-id="d8265-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d8265-115">Return code</span></span>                                                                          | <span data-ttu-id="d8265-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8265-116">Description</span></span>                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d8265-117"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="d8265-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="d8265-118">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d8265-118">The function call succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="d8265-119"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="d8265-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="d8265-120">Falha na chamada de função.</span><span class="sxs-lookup"><span data-stu-id="d8265-120">The function call failed.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="d8265-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8265-121">Remarks</span></span>

<span data-ttu-id="d8265-122">Consulte o DirectDraw Software Development Kit (SDK) e o Driver Development Kit (DDK) para obter uma descrição completa dos anexos de superfície.</span><span class="sxs-lookup"><span data-stu-id="d8265-122">See the DirectDraw  software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.</span></span>

> [!Note]  
> <span data-ttu-id="d8265-123">Assim como ocorre com outros anexos de superfície, o anexo resultante é unidirecional.</span><span class="sxs-lookup"><span data-stu-id="d8265-123">As with other surface attachments, the resulting attachment is one-way.</span></span> <span data-ttu-id="d8265-124">Depois que essa função for chamada, *hSurfaceTo* não será anexado a *hSurfaceFrom*.</span><span class="sxs-lookup"><span data-stu-id="d8265-124">After this function is called, *hSurfaceTo* will not be attached to *hSurfaceFrom*.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8265-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8265-125">Requirements</span></span>



| <span data-ttu-id="d8265-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8265-126">Requirement</span></span> | <span data-ttu-id="d8265-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d8265-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8265-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8265-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d8265-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8265-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d8265-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8265-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d8265-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8265-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d8265-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d8265-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8265-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8265-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8265-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8265-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8265-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="d8265-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




