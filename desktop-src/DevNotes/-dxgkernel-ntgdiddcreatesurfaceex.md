---
description: Cria uma superfície do Microsoft Direct3D de uma superfície do Microsoft DirectDraw e associa um valor de identificador solicitado a ela.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Função NtGdiDdCreateSurfaceEx (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088918"
---
# <a name="ntgdiddcreatesurfaceex-function"></a><span data-ttu-id="9a8ef-103">Função NtGdiDdCreateSurfaceEx</span><span class="sxs-lookup"><span data-stu-id="9a8ef-103">NtGdiDdCreateSurfaceEx function</span></span>

<span data-ttu-id="9a8ef-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9a8ef-105">Em vez disso, use o DirectDraw e o Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="9a8ef-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9a8ef-106">Cria uma superfície do Microsoft Direct3D de uma superfície do Microsoft DirectDraw e associa um valor de identificador solicitado a ela.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-106">Creates a Microsoft Direct3D surface from a Microsoft DirectDraw surface and associates a requested handle value to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a8ef-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a8ef-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a><span data-ttu-id="9a8ef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a8ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a8ef-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a8ef-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a8ef-110">Identificador para o objeto do DirectDraw criado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-110">Handle to the DirectDraw object created by the application.</span></span>

</dd> <dt>

<span data-ttu-id="9a8ef-111">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a8ef-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a8ef-112">Manipule a superfície do DirectDraw a ser criada para o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-112">Handle to the DirectDraw surface to be created for Direct3D.</span></span> <span data-ttu-id="9a8ef-113">Esses identificadores são exclusivos em cada [**estrutura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) diferente do DIRECTDRAW do DD.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-113">These handles are unique within each different [**DD\_DIRECTDRAW\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9a8ef-114">*dwSurfaceHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a8ef-114">*dwSurfaceHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a8ef-115">Identificador para uma [**estrutura \_ CREATESURFACEEXDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) que contém as informações necessárias para o driver criar a superfície.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-115">Handle to a [**DD\_CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) structure that contains the information required for the driver to create the surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a8ef-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a8ef-116">Return value</span></span>

<span data-ttu-id="9a8ef-117">**NtGdiDdCreateSurfaceEx** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-117">**NtGdiDdCreateSurfaceEx** returns one of the following callback codes.</span></span>



| <span data-ttu-id="9a8ef-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9a8ef-118">Return code</span></span>                                                                                              | <span data-ttu-id="9a8ef-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a8ef-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a8ef-120"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="9a8ef-120"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="9a8ef-121">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-121">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="9a8ef-122">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-122">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="9a8ef-123">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-123">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9a8ef-124"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="9a8ef-124"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="9a8ef-125">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-125">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="9a8ef-126">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-126">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="9a8ef-127">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a8ef-127">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9a8ef-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a8ef-128">Requirements</span></span>



| <span data-ttu-id="9a8ef-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a8ef-129">Requirement</span></span> | <span data-ttu-id="9a8ef-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9a8ef-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8ef-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a8ef-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9a8ef-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a8ef-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9a8ef-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a8ef-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9a8ef-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a8ef-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9a8ef-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9a8ef-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a8ef-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a8ef-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a8ef-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a8ef-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a8ef-138">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="9a8ef-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
