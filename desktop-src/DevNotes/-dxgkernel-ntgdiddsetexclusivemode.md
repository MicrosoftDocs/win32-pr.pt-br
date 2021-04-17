---
description: Notifica o driver quando um aplicativo Microsoft DirectDraw está alternando para ou do modo exclusivo.
ms.assetid: f2b63d90-7ede-479f-a2fd-ae9870c4d7b9
title: Função NtGdiDdSetExclusiveMode (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetExclusiveMode
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1d2420f4ae093b4bfc3f68871daefd5c20da308e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756013"
---
# <a name="ntgdiddsetexclusivemode-function"></a><span data-ttu-id="ba829-103">Função NtGdiDdSetExclusiveMode</span><span class="sxs-lookup"><span data-stu-id="ba829-103">NtGdiDdSetExclusiveMode function</span></span>

<span data-ttu-id="ba829-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ba829-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ba829-105">Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="ba829-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ba829-106">Notifica o driver quando um aplicativo Microsoft DirectDraw está alternando para ou do modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ba829-106">Notifies the driver when a Microsoft DirectDraw application is switching to or from exclusive mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba829-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba829-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetExclusiveMode(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_SETEXCLUSIVEMODEDATA puSetExclusiveModeData
);
```



## <a name="parameters"></a><span data-ttu-id="ba829-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba829-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba829-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba829-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba829-110">Identificador para objeto DirectDraw do modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ba829-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="ba829-111">*puSetExclusiveModeData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ba829-111">*puSetExclusiveModeData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba829-112">Ponteiro para uma [**estrutura \_ SETEXCLUSIVEMODEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) que contém as informações de notificação.</span><span class="sxs-lookup"><span data-stu-id="ba829-112">Pointer to a [**DD\_SETEXCLUSIVEMODEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba829-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba829-113">Return value</span></span>

<span data-ttu-id="ba829-114">**NtGdiDdSetExclusiveMode** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ba829-114">**NtGdiDdSetExclusiveMode** returns one of the following callback codes.</span></span>



| <span data-ttu-id="ba829-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ba829-115">Return code</span></span>                                                                                              | <span data-ttu-id="ba829-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba829-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba829-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="ba829-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="ba829-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="ba829-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="ba829-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="ba829-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="ba829-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="ba829-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="ba829-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="ba829-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="ba829-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ba829-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="ba829-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="ba829-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="ba829-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ba829-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ba829-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba829-125">Requirements</span></span>



| <span data-ttu-id="ba829-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba829-126">Requirement</span></span> | <span data-ttu-id="ba829-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ba829-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba829-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba829-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ba829-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba829-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ba829-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba829-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ba829-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba829-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ba829-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ba829-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba829-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba829-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba829-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba829-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba829-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="ba829-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
