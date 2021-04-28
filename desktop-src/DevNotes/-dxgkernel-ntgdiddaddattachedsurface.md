---
description: Função NtGdiDdAddAttachedSurface – anexa uma superfície a outra superfície.
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: Função NtGdiDdAddAttachedSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAddAttachedSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dacaa07a586a88c808d8da07b8233002e8ae5055
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085784"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="39bc4-103">Função NtGdiDdAddAttachedSurface</span><span class="sxs-lookup"><span data-stu-id="39bc4-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="39bc4-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="39bc4-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="39bc4-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="39bc4-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="39bc4-106">Anexa uma superfície a outra superfície.</span><span class="sxs-lookup"><span data-stu-id="39bc4-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="39bc4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39bc4-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="39bc4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39bc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bc4-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39bc4-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39bc4-110">Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa a superfície à qual outra superfície está sendo anexada.</span><span class="sxs-lookup"><span data-stu-id="39bc4-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="39bc4-111">*hSurfaceAttached* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39bc4-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39bc4-112">Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa a superfície a ser anexada.</span><span class="sxs-lookup"><span data-stu-id="39bc4-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="39bc4-113">*puAddAttachedSurfaceData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="39bc4-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39bc4-114">Ponteiro para uma [**estrutura \_ ADDATTACHEDSURFACEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) que contém informações necessárias para o driver executar o anexo.</span><span class="sxs-lookup"><span data-stu-id="39bc4-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39bc4-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="39bc4-115">Return value</span></span>

<span data-ttu-id="39bc4-116">**NtGdiDdAddAttachedSurface** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="39bc4-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="39bc4-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="39bc4-117">Return code</span></span>                                                                                              | <span data-ttu-id="39bc4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="39bc4-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39bc4-119"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="39bc4-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="39bc4-120">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="39bc4-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="39bc4-121">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="39bc4-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="39bc4-122">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="39bc4-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="39bc4-123"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="39bc4-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="39bc4-124">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="39bc4-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="39bc4-125">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="39bc4-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="39bc4-126">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39bc4-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39bc4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39bc4-127">Requirements</span></span>



| <span data-ttu-id="39bc4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="39bc4-128">Requirement</span></span> | <span data-ttu-id="39bc4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="39bc4-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39bc4-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39bc4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="39bc4-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39bc4-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="39bc4-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39bc4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="39bc4-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39bc4-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="39bc4-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="39bc4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="39bc4-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bc4-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39bc4-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="39bc4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bc4-137">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="39bc4-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
