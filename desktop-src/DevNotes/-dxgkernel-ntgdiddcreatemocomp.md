---
description: Notifica o driver de que um decodificador de software começará a usar a compensação de movimento com o GUID especificado.
ms.assetid: c9a55428-7fe6-45dd-987a-d9ab8ae8a1cb
title: Função NtGdiDdCreateMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1705b5bf7ac5eddd1ac39e14f3b91b7fd3728cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089149"
---
# <a name="ntgdiddcreatemocomp-function"></a><span data-ttu-id="1dc8a-103">Função NtGdiDdCreateMoComp</span><span class="sxs-lookup"><span data-stu-id="1dc8a-103">NtGdiDdCreateMoComp function</span></span>

<span data-ttu-id="1dc8a-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1dc8a-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="1dc8a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1dc8a-106">Notifica o driver de que um decodificador de software começará a usar a compensação de movimento com o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-106">Notifies the driver that a software decoder will start using motion compensation with the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc8a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1dc8a-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateMoComp(
  _In_    HANDLE               hDirectDraw,
  _Inout_ PDD_CREATEMOCOMPDATA puCreateMoCompData
);
```



## <a name="parameters"></a><span data-ttu-id="1dc8a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dc8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dc8a-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1dc8a-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc8a-110">Identificador para um objeto de modo de kernel do DirectDraw criado anteriormente para o dispositivo no qual a compensação de movimento deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-110">Handle to a previously created DirectDraw kernel-mode object for the device on which motion compensation is to be used.</span></span>

</dd> <dt>

<span data-ttu-id="1dc8a-111">*puCreateMoCompData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1dc8a-111">*puCreateMoCompData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dc8a-112">Ponteiro para uma [**estrutura \_ CREATEMOCOMPDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) que contém as informações necessárias para começar a usar a compensação de movimento.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-112">Pointer to a [**DD\_CREATEMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) structure that contains the information required to begin using motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dc8a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1dc8a-113">Return value</span></span>

<span data-ttu-id="1dc8a-114">**NtGdiDdCreateMoComp** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-114">**NtGdiDdCreateMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1dc8a-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1dc8a-115">Return code</span></span>                                                                                              | <span data-ttu-id="1dc8a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1dc8a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1dc8a-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="1dc8a-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1dc8a-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1dc8a-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1dc8a-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1dc8a-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="1dc8a-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1dc8a-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1dc8a-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1dc8a-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1dc8a-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1dc8a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dc8a-125">Remarks</span></span>

<span data-ttu-id="1dc8a-126">Para obter mais informações, consulte o Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="1dc8a-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc8a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dc8a-127">Requirements</span></span>



| <span data-ttu-id="1dc8a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc8a-128">Requirement</span></span> | <span data-ttu-id="1dc8a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc8a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc8a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc8a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc8a-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1dc8a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1dc8a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc8a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc8a-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1dc8a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1dc8a-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1dc8a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dc8a-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc8a-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc8a-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dc8a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc8a-137">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="1dc8a-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
