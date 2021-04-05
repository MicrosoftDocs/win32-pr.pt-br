---
description: Determina se a inversão solicitada mais recentemente em uma superfície ocorreu.
ms.assetid: 4489e259-b22d-4e72-807a-5290401f0331
title: Função NtGdiDdGetFlipStatus (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetFlipStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 49ef59fd110c315b3111252084a3c60ddf4cd598
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826374"
---
# <a name="ntgdiddgetflipstatus-function"></a><span data-ttu-id="43e18-103">Função NtGdiDdGetFlipStatus</span><span class="sxs-lookup"><span data-stu-id="43e18-103">NtGdiDdGetFlipStatus function</span></span>

<span data-ttu-id="43e18-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="43e18-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="43e18-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="43e18-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="43e18-106">Determina se a inversão solicitada mais recentemente em uma superfície ocorreu.</span><span class="sxs-lookup"><span data-stu-id="43e18-106">Determines whether the most recently requested flip on a surface has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e18-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43e18-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetFlipStatus(
  _In_    HANDLE                hSurface,
  _Inout_ PDD_GETFLIPSTATUSDATA puGetFlipStatusData
);
```



## <a name="parameters"></a><span data-ttu-id="43e18-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43e18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e18-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43e18-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e18-110">Identificador para uma [estrutura \_ \_ local de superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície cujo status de inversão está sendo consultado.</span><span class="sxs-lookup"><span data-stu-id="43e18-110">Handle to a [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure that describes the surface whose flip status is being queried.</span></span>

</dd> <dt>

<span data-ttu-id="43e18-111">*puGetFlipStatusData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="43e18-111">*puGetFlipStatusData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43e18-112">Ponteiro para uma [estrutura \_ GETFLIPSTATUSDATA do DD](https://msdn.microsoft.com/library/ms793859.aspx) que contém as informações necessárias para executar a consulta de status invertido.</span><span class="sxs-lookup"><span data-stu-id="43e18-112">Pointer to a [DD\_GETFLIPSTATUSDATA](https://msdn.microsoft.com/library/ms793859.aspx) structure that contains the information required to perform the flip status query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e18-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43e18-113">Return value</span></span>

<span data-ttu-id="43e18-114">**NtGdiDdGetFlipStatus** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="43e18-114">**NtGdiDdGetFlipStatus** returns one of the following callback codes.</span></span>



| <span data-ttu-id="43e18-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="43e18-115">Return code</span></span>                                                                                              | <span data-ttu-id="43e18-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="43e18-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43e18-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="43e18-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="43e18-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="43e18-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="43e18-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="43e18-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="43e18-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="43e18-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="43e18-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="43e18-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="43e18-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="43e18-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="43e18-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="43e18-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="43e18-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43e18-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43e18-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e18-125">Requirements</span></span>



| <span data-ttu-id="43e18-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e18-126">Requirement</span></span> | <span data-ttu-id="43e18-127">Valor</span><span class="sxs-lookup"><span data-stu-id="43e18-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43e18-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43e18-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43e18-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43e18-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="43e18-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43e18-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43e18-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43e18-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="43e18-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="43e18-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="43e18-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="43e18-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e18-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="43e18-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e18-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="43e18-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




