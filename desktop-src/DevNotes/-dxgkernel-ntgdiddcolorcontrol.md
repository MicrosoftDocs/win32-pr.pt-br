---
description: Controla os controles de luminosidade e brilho de uma superfície de sobreposição.
ms.assetid: 2f617c89-5505-4d84-be7d-473b216c0571
title: Função NtGdiDdColorControl (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdColorControl
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45ed8683a892b07fa63fbe79b657669e647126cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088923"
---
# <a name="ntgdiddcolorcontrol-function"></a><span data-ttu-id="de86e-103">Função NtGdiDdColorControl</span><span class="sxs-lookup"><span data-stu-id="de86e-103">NtGdiDdColorControl function</span></span>

<span data-ttu-id="de86e-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="de86e-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="de86e-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="de86e-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="de86e-106">Controla os controles de luminosidade e brilho de uma superfície de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="de86e-106">Controls the luminance and brightness controls of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="de86e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de86e-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdColorControl(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_COLORCONTROLDATA puColorControlData
);
```



## <a name="parameters"></a><span data-ttu-id="de86e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de86e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de86e-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="de86e-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de86e-110">Identificador para a [**estrutura \_ \_ local da superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa a superfície de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="de86e-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="de86e-111">*puColorControlData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="de86e-111">*puColorControlData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de86e-112">Ponteiro para uma [**estrutura \_ COLORCONTROLDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) que contém as informações de controle de cor para uma superfície de sobreposição especificada.</span><span class="sxs-lookup"><span data-stu-id="de86e-112">Pointer to a [**DD\_COLORCONTROLDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) structure that contains the color control information for a specified overlay surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de86e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de86e-113">Return value</span></span>

<span data-ttu-id="de86e-114">**NtGdiDdColorControl** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="de86e-114">**NtGdiDdColorControl** returns one of the following callback codes.</span></span>



| <span data-ttu-id="de86e-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="de86e-115">Return code</span></span>                                                                                              | <span data-ttu-id="de86e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="de86e-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de86e-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="de86e-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="de86e-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="de86e-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="de86e-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="de86e-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="de86e-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="de86e-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="de86e-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="de86e-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="de86e-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="de86e-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="de86e-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="de86e-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="de86e-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de86e-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="de86e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de86e-125">Requirements</span></span>



| <span data-ttu-id="de86e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="de86e-126">Requirement</span></span> | <span data-ttu-id="de86e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="de86e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de86e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de86e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="de86e-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de86e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="de86e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de86e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="de86e-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de86e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="de86e-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="de86e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="de86e-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="de86e-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de86e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="de86e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de86e-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="de86e-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
