---
description: Faz com que a memória da superfície associada ao destino e as superfícies atuais sejam trocadas.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Função NtGdiDdFlip (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826378"
---
# <a name="ntgdiddflip-function"></a><span data-ttu-id="01fe1-103">Função NtGdiDdFlip</span><span class="sxs-lookup"><span data-stu-id="01fe1-103">NtGdiDdFlip function</span></span>

<span data-ttu-id="01fe1-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="01fe1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="01fe1-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="01fe1-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="01fe1-106">Faz com que a memória da superfície associada ao destino e as superfícies atuais sejam trocadas.</span><span class="sxs-lookup"><span data-stu-id="01fe1-106">Causes the surface memory associated with the target and current surfaces to be interchanged.</span></span>

## <a name="syntax"></a><span data-ttu-id="01fe1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01fe1-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a><span data-ttu-id="01fe1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01fe1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fe1-109">*hSurfaceCurrent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01fe1-109">*hSurfaceCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fe1-110">Identificador para a [estrutura \_ \_ local da superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície atual.</span><span class="sxs-lookup"><span data-stu-id="01fe1-110">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current surface.</span></span>

</dd> <dt>

<span data-ttu-id="01fe1-111">*hSurfaceTarget* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01fe1-111">*hSurfaceTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fe1-112">Manipule a estrutura [ \_ \_ local da superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície de destino; ou seja, a superfície à qual o driver deve ser invertido.</span><span class="sxs-lookup"><span data-stu-id="01fe1-112">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the target surface; that is, the surface to which the driver should flip.</span></span>

</dd> <dt>

<span data-ttu-id="01fe1-113">*hSurfaceCurrentLeft* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01fe1-113">*hSurfaceCurrentLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fe1-114">Manipule a estrutura [ \_ \_ local da superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície esquerda atual.</span><span class="sxs-lookup"><span data-stu-id="01fe1-114">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current left surface.</span></span>

</dd> <dt>

<span data-ttu-id="01fe1-115">*hSurfaceTargetLeft* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01fe1-115">*hSurfaceTargetLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01fe1-116">Manipule a estrutura [ \_ \_ local da superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície de destino à esquerda para virar.</span><span class="sxs-lookup"><span data-stu-id="01fe1-116">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the left target surface to flip to.</span></span>

</dd> <dt>

<span data-ttu-id="01fe1-117">*puFlipData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="01fe1-117">*puFlipData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01fe1-118">Ponteiro para uma [estrutura \_ FLIPDATA do DD](https://msdn.microsoft.com/library/ms794213.aspx) que contém as informações necessárias para executar a inversão.</span><span class="sxs-lookup"><span data-stu-id="01fe1-118">Pointer to a [DD\_FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) structure that contains the information required to perform the flip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fe1-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01fe1-119">Return value</span></span>

<span data-ttu-id="01fe1-120">**NtGdiDdFlip** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="01fe1-120">**NtGdiDdFlip** returns one of the following callback codes.</span></span>



| <span data-ttu-id="01fe1-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01fe1-121">Return code</span></span>                                                                                              | <span data-ttu-id="01fe1-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="01fe1-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01fe1-123"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="01fe1-123"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="01fe1-124">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="01fe1-124">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="01fe1-125">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="01fe1-125">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="01fe1-126">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="01fe1-126">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="01fe1-127"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="01fe1-127"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="01fe1-128">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="01fe1-128">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="01fe1-129">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="01fe1-129">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="01fe1-130">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01fe1-130">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="01fe1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01fe1-131">Requirements</span></span>



| <span data-ttu-id="01fe1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="01fe1-132">Requirement</span></span> | <span data-ttu-id="01fe1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="01fe1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01fe1-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01fe1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="01fe1-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01fe1-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="01fe1-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01fe1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="01fe1-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01fe1-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="01fe1-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="01fe1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="01fe1-139"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="01fe1-139"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01fe1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="01fe1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01fe1-141">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="01fe1-141">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




