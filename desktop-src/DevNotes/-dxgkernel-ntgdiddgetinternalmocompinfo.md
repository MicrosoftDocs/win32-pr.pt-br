---
description: Permite que o driver relate que internamente aloca memória de vídeo para executar a compensação de movimento.
ms.assetid: cf2878ae-7eff-4214-bb9e-e8b608831108
title: Função NtGdiDdGetInternalMoCompInfo (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetInternalMoCompInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a9ddbb7843c7a1142ac6cd9906ef1ed3265e5d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826373"
---
# <a name="ntgdiddgetinternalmocompinfo-function"></a><span data-ttu-id="281d8-103">Função NtGdiDdGetInternalMoCompInfo</span><span class="sxs-lookup"><span data-stu-id="281d8-103">NtGdiDdGetInternalMoCompInfo function</span></span>

<span data-ttu-id="281d8-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="281d8-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="281d8-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="281d8-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="281d8-106">Permite que o driver relate que internamente aloca memória de vídeo para executar a compensação de movimento.</span><span class="sxs-lookup"><span data-stu-id="281d8-106">Allows the driver to report that it internally allocates display memory to perform motion compensation.</span></span>

## <a name="syntax"></a><span data-ttu-id="281d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="281d8-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetInternalMoCompInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETINTERNALMOCOMPDATA puGetInternalData
);
```



## <a name="parameters"></a><span data-ttu-id="281d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="281d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="281d8-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="281d8-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="281d8-110">Identificador para objeto DirectDraw do modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="281d8-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="281d8-111">*puGetInternalData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="281d8-111">*puGetInternalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="281d8-112">Ponteiro para uma [**estrutura \_ GETINTERNALMOCOMPDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) que contém os requisitos de memória interna.</span><span class="sxs-lookup"><span data-stu-id="281d8-112">Pointer to a [**DD\_GETINTERNALMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) structure that contains the internal memory requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="281d8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="281d8-113">Return value</span></span>

<span data-ttu-id="281d8-114">**NtGdiDdGetInternalMoCompInfo** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="281d8-114">**NtGdiDdGetInternalMoCompInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="281d8-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="281d8-115">Return code</span></span>                                                                                              | <span data-ttu-id="281d8-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="281d8-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="281d8-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="281d8-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="281d8-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="281d8-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="281d8-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="281d8-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="281d8-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="281d8-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="281d8-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="281d8-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="281d8-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="281d8-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="281d8-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="281d8-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="281d8-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="281d8-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="281d8-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="281d8-125">Remarks</span></span>

<span data-ttu-id="281d8-126">Para obter mais informações, consulte o Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="281d8-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="281d8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="281d8-127">Requirements</span></span>



| <span data-ttu-id="281d8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="281d8-128">Requirement</span></span> | <span data-ttu-id="281d8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="281d8-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="281d8-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="281d8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="281d8-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="281d8-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="281d8-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="281d8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="281d8-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="281d8-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="281d8-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="281d8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="281d8-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="281d8-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="281d8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="281d8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281d8-137">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="281d8-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
