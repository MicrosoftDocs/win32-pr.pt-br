---
description: Indica se o driver pode criar uma superfície da descrição da superfície especificada.
ms.assetid: 4626163b-3070-4246-9a04-0b3438fc7057
title: Função NtGdiDdCanCreateSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCanCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c45f3e93bff409f68e5ba7fbe441a398e80b0e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456914"
---
# <a name="ntgdiddcancreatesurface-function"></a><span data-ttu-id="19799-103">Função NtGdiDdCanCreateSurface</span><span class="sxs-lookup"><span data-stu-id="19799-103">NtGdiDdCanCreateSurface function</span></span>

<span data-ttu-id="19799-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="19799-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="19799-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="19799-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="19799-106">Indica se o driver pode criar uma superfície da descrição da superfície especificada.</span><span class="sxs-lookup"><span data-stu-id="19799-106">Indicates whether the driver can create a surface of the specified surface description.</span></span>

## <a name="syntax"></a><span data-ttu-id="19799-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19799-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCanCreateSurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_CANCREATESURFACEDATA puCanCreateSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="19799-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19799-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19799-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="19799-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19799-110">Identificador para a [**estrutura \_ \_ global do DIRECTDRAW do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa o objeto DIRECTDRAW.</span><span class="sxs-lookup"><span data-stu-id="19799-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="19799-111">*puCanCreateSurfaceData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="19799-111">*puCanCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19799-112">Ponteiro para uma [**estrutura \_ CANCREATESURFACEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) que contém as informações necessárias para o driver determinar se uma superfície pode ser criada.</span><span class="sxs-lookup"><span data-stu-id="19799-112">Pointer to a [**DD\_CANCREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata) structure containing the information required for the driver to determine whether a surface can be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19799-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19799-113">Return value</span></span>

<span data-ttu-id="19799-114">**NtGdiDdCanCreateSurface** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="19799-114">**NtGdiDdCanCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="19799-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="19799-115">Return code</span></span>                                                                                              | <span data-ttu-id="19799-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="19799-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="19799-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="19799-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="19799-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="19799-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="19799-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="19799-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="19799-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="19799-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="19799-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="19799-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="19799-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="19799-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="19799-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="19799-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="19799-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="19799-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19799-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19799-125">Requirements</span></span>



| <span data-ttu-id="19799-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="19799-126">Requirement</span></span> | <span data-ttu-id="19799-127">Valor</span><span class="sxs-lookup"><span data-stu-id="19799-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19799-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19799-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19799-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="19799-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="19799-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19799-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19799-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="19799-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="19799-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="19799-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="19799-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19799-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19799-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="19799-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19799-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="19799-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
