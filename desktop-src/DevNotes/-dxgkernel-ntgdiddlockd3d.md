---
description: Usado para bloquear uma área especificada de memória de buffer e fornecer um ponteiro válido para um bloco de memória associado ao buffer.
ms.assetid: 6f2ecefa-376c-4f6c-a031-666dd992f96a
title: Função NtGdiDdLockD3D (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLockD3D
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c049d37e3507f5bf4429b6ffd5d8ec03327640e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750291"
---
# <a name="ntgdiddlockd3d-function"></a><span data-ttu-id="a36f7-103">Função NtGdiDdLockD3D</span><span class="sxs-lookup"><span data-stu-id="a36f7-103">NtGdiDdLockD3D function</span></span>

<span data-ttu-id="a36f7-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a36f7-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="a36f7-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="a36f7-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="a36f7-106">Usado para bloquear uma área especificada de memória de buffer e fornecer um ponteiro válido para um bloco de memória associado ao buffer.</span><span class="sxs-lookup"><span data-stu-id="a36f7-106">Used to lock a specified area of buffer memory and to provide a valid pointer to a block of memory associated with the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a36f7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a36f7-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLockD3D(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData
);
```



## <a name="parameters"></a><span data-ttu-id="a36f7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a36f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a36f7-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a36f7-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a36f7-110">Ponteiro para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície associada à região da memória a ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a36f7-110">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="a36f7-111">*puLockData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a36f7-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a36f7-112">Ponteiro para uma [**estrutura \_ LOCKDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) que contém as informações necessárias para executar o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a36f7-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lock down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a36f7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a36f7-113">Return value</span></span>

<span data-ttu-id="a36f7-114">**NtGdiDdLockD3D** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a36f7-114">**NtGdiDdLockD3D** returns one of the following callback codes.</span></span>



| <span data-ttu-id="a36f7-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a36f7-115">Return code</span></span>                                                                                              | <span data-ttu-id="a36f7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a36f7-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a36f7-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="a36f7-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="a36f7-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="a36f7-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="a36f7-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="a36f7-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="a36f7-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="a36f7-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a36f7-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="a36f7-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="a36f7-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="a36f7-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="a36f7-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="a36f7-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="a36f7-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a36f7-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a36f7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a36f7-125">Requirements</span></span>



| <span data-ttu-id="a36f7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a36f7-126">Requirement</span></span> | <span data-ttu-id="a36f7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a36f7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a36f7-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a36f7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a36f7-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a36f7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a36f7-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a36f7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a36f7-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a36f7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a36f7-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a36f7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a36f7-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a36f7-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a36f7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a36f7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a36f7-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="a36f7-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
