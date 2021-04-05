---
description: Notifica o driver de que este objeto de compensação de movimento não será mais usado. O driver agora precisa executar qualquer limpeza necessária.
ms.assetid: 1d86a564-efe1-4971-99ec-2c9a6aa59c89
title: Função NtGdiDdDestroyMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: b7bc5915fe43bd4d48495b2b1beda8ee38f05fe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826287"
---
# <a name="ntgdidddestroymocomp-function"></a><span data-ttu-id="4e311-104">Função NtGdiDdDestroyMoComp</span><span class="sxs-lookup"><span data-stu-id="4e311-104">NtGdiDdDestroyMoComp function</span></span>

<span data-ttu-id="4e311-105">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4e311-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="4e311-106">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="4e311-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="4e311-107">Notifica o driver de que este objeto de compensação de movimento não será mais usado.</span><span class="sxs-lookup"><span data-stu-id="4e311-107">Notifies the driver that this motion compensation object will no longer be used.</span></span> <span data-ttu-id="4e311-108">O driver agora precisa executar qualquer limpeza necessária.</span><span class="sxs-lookup"><span data-stu-id="4e311-108">The driver now needs to perform any necessary cleanup.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e311-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e311-109">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyMoComp(
  _In_    HANDLE                hMoComp,
  _Inout_ PDD_DESTROYMOCOMPDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="4e311-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e311-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e311-111">*hMoComp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e311-111">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e311-112">Identificador para uma [**estrutura \_ \_ local MOTIONCOMP DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contém uma descrição do objeto de compensação de movimento a ser destruído.</span><span class="sxs-lookup"><span data-stu-id="4e311-112">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation object to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="4e311-113">*puBeginFrameData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4e311-113">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e311-114">Ponteiro para uma [**estrutura \_ DESTROYMOCOMPDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) que contém as informações necessárias para concluir a compensação de movimento.</span><span class="sxs-lookup"><span data-stu-id="4e311-114">Pointer to a [**DD\_DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) structure that contains the information needed to finish motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e311-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e311-115">Return value</span></span>

<span data-ttu-id="4e311-116">**NtGdiDdDestroyMoComp** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="4e311-116">**NtGdiDdDestroyMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="4e311-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4e311-117">Return code</span></span>                                                                                              | <span data-ttu-id="4e311-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e311-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e311-119"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="4e311-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="4e311-120">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="4e311-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="4e311-121">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="4e311-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="4e311-122">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="4e311-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="4e311-123"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="4e311-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="4e311-124">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="4e311-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="4e311-125">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="4e311-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="4e311-126">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4e311-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e311-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e311-127">Remarks</span></span>

<span data-ttu-id="4e311-128">Para obter mais informações, consulte o Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="4e311-128">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e311-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e311-129">Requirements</span></span>



| <span data-ttu-id="4e311-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e311-130">Requirement</span></span> | <span data-ttu-id="4e311-131">Valor</span><span class="sxs-lookup"><span data-stu-id="4e311-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e311-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e311-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4e311-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e311-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4e311-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e311-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4e311-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e311-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4e311-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e311-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e311-137"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e311-137"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e311-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e311-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e311-139">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="4e311-139">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
