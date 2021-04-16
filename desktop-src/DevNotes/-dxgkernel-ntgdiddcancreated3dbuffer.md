---
description: Determina se o driver pode criar um buffer de vértice ou comando no nível do driver da descrição especificada.
ms.assetid: c67492d9-c4ba-4206-8beb-3d67235192f9
title: Função NtGdiDdCanCreateD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 849eb2ba9c1349c54c20703217989b0b92ee78e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752600"
---
# <a name="ntgdiddcancreated3dbuffer-function"></a><span data-ttu-id="bb6f4-103">Função NtGdiDdCanCreateD3DBuffer</span><span class="sxs-lookup"><span data-stu-id="bb6f4-103">NtGdiDdCanCreateD3DBuffer function</span></span>

<span data-ttu-id="bb6f4-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="bb6f4-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="bb6f4-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="bb6f4-106">Determina se o driver pode criar um buffer de vértice ou comando no nível do driver da descrição especificada.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-106">Determines whether the driver can create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6f4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb6f4-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateD3DBuffer(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="bb6f4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb6f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb6f4-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb6f4-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6f4-110">Identificador para a [**estrutura \_ \_ global do DIRECTDRAW do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa o objeto DIRECTDRAW.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="bb6f4-111">*puCanCreateSurfaceData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bb6f4-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6f4-112">Ponteiro para uma [**estrutura \_ CANCREATESURFACEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) .</span><span class="sxs-lookup"><span data-stu-id="bb6f4-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure.</span></span> <span data-ttu-id="bb6f4-113">Essa estrutura contém as informações necessárias para o driver determinar se um buffer de comando ou vértice pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-113">This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb6f4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb6f4-114">Return value</span></span>

<span data-ttu-id="bb6f4-115">**NtGdiDdCanCreateD3DBuffer** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-115">**NtGdiDdCanCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="bb6f4-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bb6f4-116">Return code</span></span>                                                                                              | <span data-ttu-id="bb6f4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb6f4-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb6f4-118"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6f4-118"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="bb6f4-119">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-119">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="bb6f4-120">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-120">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="bb6f4-121">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-121">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="bb6f4-122"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6f4-122"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="bb6f4-123">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-123">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="bb6f4-124">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-124">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="bb6f4-125">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb6f4-125">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb6f4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb6f4-126">Requirements</span></span>



| <span data-ttu-id="bb6f4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb6f4-127">Requirement</span></span> | <span data-ttu-id="bb6f4-128">Valor</span><span class="sxs-lookup"><span data-stu-id="bb6f4-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6f4-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb6f4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6f4-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bb6f4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bb6f4-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb6f4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6f4-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bb6f4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb6f4-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bb6f4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb6f4-134"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6f4-134"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb6f4-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb6f4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6f4-136">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="bb6f4-136">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
