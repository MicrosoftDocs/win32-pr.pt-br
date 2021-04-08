---
description: Reposiciona ou modifica os atributos visuais de uma superfície de sobreposição.
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: Função NtGdiDdUpdateOverlay (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bbe610c27d83061bda0996ce9acc082efa95e3a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920166"
---
# <a name="ntgdiddupdateoverlay-function"></a><span data-ttu-id="6c5c3-103">Função NtGdiDdUpdateOverlay</span><span class="sxs-lookup"><span data-stu-id="6c5c3-103">NtGdiDdUpdateOverlay function</span></span>

<span data-ttu-id="6c5c3-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="6c5c3-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="6c5c3-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="6c5c3-106">Reposiciona ou modifica os atributos visuais de uma superfície de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-106">Repositions or modifies the visual attributes of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5c3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c5c3-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a><span data-ttu-id="6c5c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c5c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5c3-109">*hSurfaceDestination* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c5c3-109">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5c3-110">Identificador para objeto DirectDraw do modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="6c5c3-111">*hSurfaceSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c5c3-111">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5c3-112">Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="6c5c3-113">*puUpdateOverlayData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6c5c3-113">*puUpdateOverlayData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5c3-114">Ponteiro para uma [**estrutura \_ UPDATEOVERLAYDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) que contém as informações necessárias para atualizar a sobreposição.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-114">Pointer to a [**DD\_UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) structure that contains the information required to update the overlay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5c3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c5c3-115">Return value</span></span>

<span data-ttu-id="6c5c3-116">**NtGdiDdUpdateOverlay** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-116">**NtGdiDdUpdateOverlay** returns one of the following callback codes.</span></span>



| <span data-ttu-id="6c5c3-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6c5c3-117">Return code</span></span>                                                                                              | <span data-ttu-id="6c5c3-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c5c3-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c5c3-119"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="6c5c3-120">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="6c5c3-121">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="6c5c3-122">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6c5c3-123"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="6c5c3-124">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="6c5c3-125">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="6c5c3-126">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c5c3-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6c5c3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c5c3-127">Requirements</span></span>



| <span data-ttu-id="6c5c3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c5c3-128">Requirement</span></span> | <span data-ttu-id="6c5c3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6c5c3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5c3-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c5c3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5c3-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c5c3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6c5c3-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c5c3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5c3-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c5c3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c5c3-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c5c3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5c3-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5c3-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5c3-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c5c3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5c3-137">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="6c5c3-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
