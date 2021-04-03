---
description: Conclui um quadro decodificado.
ms.assetid: 476f8bcc-2a93-430e-bda5-33102e36a35a
title: Função NtGdiDdEndMoCompFrame (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdEndMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 50f56faa724f88e16ef10b46342d8dd53afaf497
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646357"
---
# <a name="ntgdiddendmocompframe-function"></a><span data-ttu-id="379cb-103">Função NtGdiDdEndMoCompFrame</span><span class="sxs-lookup"><span data-stu-id="379cb-103">NtGdiDdEndMoCompFrame function</span></span>

<span data-ttu-id="379cb-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="379cb-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="379cb-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="379cb-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="379cb-106">Conclui um quadro decodificado.</span><span class="sxs-lookup"><span data-stu-id="379cb-106">Completes a decoded frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="379cb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="379cb-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdEndMoCompFrame(
  _In_    HANDLE                 hMoComp,
  _Inout_ PDD_ENDMOCOMPFRAMEDATA puEndFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="379cb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="379cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="379cb-109">*hMoComp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="379cb-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="379cb-110">Identificador para uma [estrutura \_ \_ local MOTIONCOMP DD](https://msdn.microsoft.com/library/ms794211.aspx) que contém uma descrição da compensação de movimento que está sendo solicitada.</span><span class="sxs-lookup"><span data-stu-id="379cb-110">Handle to a [DD\_MOTIONCOMP\_LOCAL](https://msdn.microsoft.com/library/ms794211.aspx) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-111">*puEndFrameData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="379cb-111">*puEndFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="379cb-112">Ponteiro para uma [estrutura \_ ENDMOCOMPFRAMEDATA do DD](https://msdn.microsoft.com/library/ms793897.aspx) que contém as informações necessárias para concluir o quadro decodificado.</span><span class="sxs-lookup"><span data-stu-id="379cb-112">Pointer to a [DD\_ENDMOCOMPFRAMEDATA](https://msdn.microsoft.com/library/ms793897.aspx) structure that contains the information needed to complete the decoded frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="379cb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="379cb-113">Return value</span></span>

<span data-ttu-id="379cb-114">**NtGdiDdEndMoCompFrame** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="379cb-114">**NtGdiDdEndMoCompFrame** returns one of the following callback codes.</span></span>



| <span data-ttu-id="379cb-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="379cb-115">Return code</span></span>                                                                                              | <span data-ttu-id="379cb-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="379cb-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="379cb-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="379cb-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="379cb-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="379cb-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="379cb-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="379cb-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="379cb-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="379cb-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="379cb-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="379cb-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="379cb-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="379cb-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="379cb-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="379cb-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="379cb-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="379cb-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="379cb-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="379cb-125">Remarks</span></span>

<span data-ttu-id="379cb-126">Para obter mais informações, consulte o Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="379cb-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="379cb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="379cb-127">Requirements</span></span>



| <span data-ttu-id="379cb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="379cb-128">Requirement</span></span> | <span data-ttu-id="379cb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="379cb-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="379cb-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="379cb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="379cb-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="379cb-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="379cb-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="379cb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="379cb-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="379cb-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="379cb-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="379cb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="379cb-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="379cb-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="379cb-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="379cb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="379cb-137">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="379cb-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




