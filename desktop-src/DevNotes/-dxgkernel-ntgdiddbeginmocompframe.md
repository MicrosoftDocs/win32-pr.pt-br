---
description: Inicia a decodificação de um novo quadro.
ms.assetid: da2c231d-89a9-4fd9-99b5-f7c1309c26e0
title: Função NtGdiDdBeginMoCompFrame (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBeginMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45c359092d1a161aae7671c437fdb9683a2a8eb9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500834"
---
# <a name="ntgdiddbeginmocompframe-function"></a><span data-ttu-id="db96c-103">Função NtGdiDdBeginMoCompFrame</span><span class="sxs-lookup"><span data-stu-id="db96c-103">NtGdiDdBeginMoCompFrame function</span></span>

<span data-ttu-id="db96c-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="db96c-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="db96c-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="db96c-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="db96c-106">Inicia a decodificação de um novo quadro.</span><span class="sxs-lookup"><span data-stu-id="db96c-106">Starts decoding a new frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="db96c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db96c-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdBeginMoCompFrame(
  _In_    HANDLE                   hMoComp,
  _Inout_ PDD_BEGINMOCOMPFRAMEDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="db96c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db96c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db96c-109">*hMoComp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db96c-109">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db96c-110">Identificador para uma [**estrutura \_ \_ local MOTIONCOMP DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contém uma descrição da compensação de movimento que está sendo solicitada.</span><span class="sxs-lookup"><span data-stu-id="db96c-110">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation being requested.</span></span>

</dd> <dt>

<span data-ttu-id="db96c-111">*puBeginFrameData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="db96c-111">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db96c-112">Ponteiro para uma [**estrutura \_ BEGINMOCOMPFRAMEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) que contém as informações necessárias para iniciar a decodificação de um novo quadro.</span><span class="sxs-lookup"><span data-stu-id="db96c-112">Pointer to a [**DD\_BEGINMOCOMPFRAMEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) structure that contains the information needed to start decoding a new frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db96c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db96c-113">Return value</span></span>

<span data-ttu-id="db96c-114">**NtGdiDdBeginMoCompFrame** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="db96c-114">**NtGdiDdBeginMoCompFrame** returns one of the following callback codes.</span></span>



| <span data-ttu-id="db96c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="db96c-115">Return code</span></span>                                                                                              | <span data-ttu-id="db96c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="db96c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db96c-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="db96c-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="db96c-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="db96c-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="db96c-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="db96c-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="db96c-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="db96c-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="db96c-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="db96c-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="db96c-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="db96c-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="db96c-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="db96c-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="db96c-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db96c-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db96c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="db96c-125">Remarks</span></span>

<span data-ttu-id="db96c-126">Para obter mais informações, consulte o Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="db96c-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="db96c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db96c-127">Requirements</span></span>



| <span data-ttu-id="db96c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="db96c-128">Requirement</span></span> | <span data-ttu-id="db96c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="db96c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db96c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db96c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="db96c-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="db96c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="db96c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db96c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="db96c-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="db96c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="db96c-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="db96c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="db96c-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="db96c-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db96c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="db96c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db96c-137">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="db96c-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
