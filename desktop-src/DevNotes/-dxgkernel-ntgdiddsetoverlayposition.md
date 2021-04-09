---
description: Define a posição de uma sobreposição.
ms.assetid: dd495118-9ceb-4100-a7ec-794659bb4461
title: Função NtGdiDdSetOverlayPosition (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetOverlayPosition
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73882e20fd7065d208835c2005d102b1312e8ce1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010109"
---
# <a name="ntgdiddsetoverlayposition-function"></a><span data-ttu-id="7c79c-103">Função NtGdiDdSetOverlayPosition</span><span class="sxs-lookup"><span data-stu-id="7c79c-103">NtGdiDdSetOverlayPosition function</span></span>

<span data-ttu-id="7c79c-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7c79c-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="7c79c-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="7c79c-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="7c79c-106">Define a posição de uma sobreposição.</span><span class="sxs-lookup"><span data-stu-id="7c79c-106">Sets the position for an overlay.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c79c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c79c-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetOverlayPosition(
  _In_    HANDLE                     hSurfaceSource,
  _In_    HANDLE                     hSurfaceDestination,
  _Inout_ PDD_SETOVERLAYPOSITIONDATA puSetOverlayPositionData
);
```



## <a name="parameters"></a><span data-ttu-id="7c79c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c79c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c79c-109">*hSurfaceSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c79c-109">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c79c-110">Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa a superfície de sobreposição do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="7c79c-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="7c79c-111">*hSurfaceDestination* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c79c-111">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c79c-112">Ponteiro para uma [**estrutura \_ \_ local de superfície DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa a superfície que está sendo sobreposta.</span><span class="sxs-lookup"><span data-stu-id="7c79c-112">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the surface that is being overlaid.</span></span>

</dd> <dt>

<span data-ttu-id="7c79c-113">*puSetOverlayPositionData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7c79c-113">*puSetOverlayPositionData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c79c-114">Ponteiro para uma [**estrutura \_ SETOVERLAYPOSITIONDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) que contém as informações necessárias para definir a posição da sobreposição.</span><span class="sxs-lookup"><span data-stu-id="7c79c-114">Pointer to a [**DD\_SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) structure that contains the information required to set the overlay position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c79c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c79c-115">Return value</span></span>

<span data-ttu-id="7c79c-116">**NtGdiDdSetOverlayPosition** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7c79c-116">**NtGdiDdSetOverlayPosition** returns one of the following callback codes.</span></span>



| <span data-ttu-id="7c79c-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7c79c-117">Return code</span></span>                                                                                              | <span data-ttu-id="7c79c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c79c-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c79c-119"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="7c79c-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="7c79c-120">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="7c79c-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="7c79c-121">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="7c79c-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="7c79c-122">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="7c79c-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7c79c-123"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="7c79c-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="7c79c-124">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="7c79c-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="7c79c-125">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="7c79c-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="7c79c-126">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c79c-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c79c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c79c-127">Requirements</span></span>



| <span data-ttu-id="7c79c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c79c-128">Requirement</span></span> | <span data-ttu-id="7c79c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7c79c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c79c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c79c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7c79c-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c79c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7c79c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c79c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7c79c-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c79c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7c79c-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c79c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c79c-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c79c-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c79c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c79c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c79c-137">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="7c79c-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
