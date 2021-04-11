---
description: Usado para liberar um bloqueio mantido em uma área especificada da memória de buffer.
ms.assetid: ec06829b-2b3a-45db-9ecd-d4c7cf67b8ae
title: Função NtGdiDdUnlockD3D (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnlockD3D
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 207f647cadc81a797d71a607fdfd6f73ea38f475
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088911"
---
# <a name="ntgdiddunlockd3d-function"></a><span data-ttu-id="cdd19-103">Função NtGdiDdUnlockD3D</span><span class="sxs-lookup"><span data-stu-id="cdd19-103">NtGdiDdUnlockD3D function</span></span>

<span data-ttu-id="cdd19-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cdd19-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="cdd19-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="cdd19-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="cdd19-106">Usado para liberar um bloqueio mantido em uma área especificada da memória de buffer.</span><span class="sxs-lookup"><span data-stu-id="cdd19-106">Used to release a lock held on a specified area of buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd19-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdd19-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUnlockD3D(
  _In_    HANDLE         hSurface,
  _Inout_ PDD_UNLOCKDATA puUnlockData
);
```



## <a name="parameters"></a><span data-ttu-id="cdd19-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdd19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd19-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cdd19-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd19-110">Ponteiro para uma [**estrutura \_ \_ local de superfície DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície a ser desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="cdd19-110">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface to be unlocked.</span></span>

</dd> <dt>

<span data-ttu-id="cdd19-111">*puUnlockData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="cdd19-111">*puUnlockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd19-112">Ponteiro para uma [**estrutura \_ UNLOCKDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) que contém as informações necessárias para executar a liberação de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="cdd19-112">Pointer to a [**DD\_UNLOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) structure that contains the information required to perform the lock release.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd19-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cdd19-113">Return value</span></span>

<span data-ttu-id="cdd19-114">**NtGdiDdUnlockD3D** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="cdd19-114">**NtGdiDdUnlockD3D** returns one of the following callback codes.</span></span>



| <span data-ttu-id="cdd19-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cdd19-115">Return code</span></span>                                                                                              | <span data-ttu-id="cdd19-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdd19-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cdd19-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="cdd19-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="cdd19-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="cdd19-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="cdd19-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="cdd19-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="cdd19-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="cdd19-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="cdd19-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="cdd19-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="cdd19-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="cdd19-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="cdd19-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="cdd19-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="cdd19-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdd19-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cdd19-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdd19-125">Requirements</span></span>



| <span data-ttu-id="cdd19-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdd19-126">Requirement</span></span> | <span data-ttu-id="cdd19-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cdd19-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd19-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdd19-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd19-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdd19-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cdd19-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdd19-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd19-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdd19-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cdd19-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cdd19-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdd19-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdd19-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd19-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdd19-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd19-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="cdd19-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
