---
description: Remove um anexo, criado com NtGdiDdAttachSurface, entre dois objetos de superfície de modo kernel.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: Função NtGdiDdUnattachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920167"
---
# <a name="ntgdiddunattachsurface-function"></a><span data-ttu-id="2b073-103">Função NtGdiDdUnattachSurface</span><span class="sxs-lookup"><span data-stu-id="2b073-103">NtGdiDdUnattachSurface function</span></span>

<span data-ttu-id="2b073-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2b073-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="2b073-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="2b073-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="2b073-106">Remove um anexo, criado com [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), entre dois objetos de superfície de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="2b073-106">Removes an attachment, created with [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), between two kernel-mode surface objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b073-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b073-107">Syntax</span></span>


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a><span data-ttu-id="2b073-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b073-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b073-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b073-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b073-110">O objeto de superfície do modo kernel que foi passado como o parâmetro hSurfaceFrom para [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span><span class="sxs-lookup"><span data-stu-id="2b073-110">The kernel-mode surface object that was passed as the hSurfaceFrom parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b073-111">*hSurfaceAttached* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2b073-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b073-112">O objeto de superfície do modo kernel que foi passado como o parâmetro hSurfaceTo para [ **NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span><span class="sxs-lookup"><span data-stu-id="2b073-112">The kernel-mode surface object that was passed as the hSurfaceTo parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b073-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b073-113">Return value</span></span>

<span data-ttu-id="2b073-114">**NtGdiDdUnattachSurface** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="2b073-114">**NtGdiDdUnattachSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="2b073-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2b073-115">Return code</span></span>                                                                                              | <span data-ttu-id="2b073-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b073-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b073-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="2b073-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="2b073-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="2b073-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="2b073-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="2b073-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="2b073-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="2b073-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="2b073-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="2b073-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="2b073-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="2b073-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="2b073-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="2b073-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="2b073-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b073-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b073-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b073-125">Remarks</span></span>

<span data-ttu-id="2b073-126">É recomendável que os aplicativos usem a API do DirectDraw, que manipula os anexos de superfície de maneira mais detalhada.</span><span class="sxs-lookup"><span data-stu-id="2b073-126">It is recommended that applications use the DirectDraw  API, which handles surface attachments in a higher-level manner.</span></span>

<span data-ttu-id="2b073-127">Não é necessário chamar essa função, pois o kernel destruirá automaticamente todos os anexos quando [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="2b073-127">It is not necessary to call this function because the kernel will automatically destroy all attachments when [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b073-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b073-128">Requirements</span></span>



| <span data-ttu-id="2b073-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b073-129">Requirement</span></span> | <span data-ttu-id="2b073-130">Valor</span><span class="sxs-lookup"><span data-stu-id="2b073-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b073-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b073-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2b073-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2b073-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2b073-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b073-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2b073-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2b073-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2b073-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2b073-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b073-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b073-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b073-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b073-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b073-138">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="2b073-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




