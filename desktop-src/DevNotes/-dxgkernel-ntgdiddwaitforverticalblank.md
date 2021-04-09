---
description: Retorna o status vertical em branco do dispositivo.
ms.assetid: d09b684b-3482-424d-8a60-d123a65f9053
title: Função NtGdiDdWaitForVerticalBlank (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdWaitForVerticalBlank
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: d138480e4a45a2b2cb67ece44ab8ceb67efae72d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088910"
---
# <a name="ntgdiddwaitforverticalblank-function"></a><span data-ttu-id="344d2-103">Função NtGdiDdWaitForVerticalBlank</span><span class="sxs-lookup"><span data-stu-id="344d2-103">NtGdiDdWaitForVerticalBlank function</span></span>

<span data-ttu-id="344d2-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="344d2-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="344d2-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="344d2-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="344d2-106">Retorna o status vertical em branco do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="344d2-106">Returns the vertical blank status of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="344d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="344d2-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdWaitForVerticalBlank(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_WAITFORVERTICALBLANKDATA puWaitForVerticalBlankData
);
```



## <a name="parameters"></a><span data-ttu-id="344d2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="344d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="344d2-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="344d2-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="344d2-110">Identificador para objeto DirectDraw do modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="344d2-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="344d2-111">*puWaitForVerticalBlankData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="344d2-111">*puWaitForVerticalBlankData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="344d2-112">Ponteiro para uma [**estrutura \_ WAITFORVERTICALBLANKDATA do DD**](/windows/win32/api/ddrawi/ns-ddrawi-ddhal_waitforverticalblankdata) que contém as informações necessárias para obter o status vertical em branco.</span><span class="sxs-lookup"><span data-stu-id="344d2-112">Pointer to a [**DD\_WAITFORVERTICALBLANKDATA**](/windows/win32/api/ddrawi/ns-ddrawi-ddhal_waitforverticalblankdata) structure that contains the information required to obtain the vertical blank status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="344d2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="344d2-113">Return value</span></span>

<span data-ttu-id="344d2-114">**NtGdiDdWaitForVerticalBlank** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="344d2-114">**NtGdiDdWaitForVerticalBlank** returns one of the following callback codes.</span></span>



| <span data-ttu-id="344d2-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="344d2-115">Return code</span></span>                                                                                              | <span data-ttu-id="344d2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="344d2-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="344d2-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="344d2-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="344d2-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="344d2-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="344d2-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="344d2-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="344d2-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="344d2-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="344d2-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="344d2-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="344d2-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="344d2-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="344d2-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="344d2-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="344d2-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="344d2-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="344d2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="344d2-125">Requirements</span></span>



| <span data-ttu-id="344d2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="344d2-126">Requirement</span></span> | <span data-ttu-id="344d2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="344d2-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="344d2-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="344d2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="344d2-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="344d2-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="344d2-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="344d2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="344d2-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="344d2-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="344d2-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="344d2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="344d2-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="344d2-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="344d2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="344d2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344d2-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="344d2-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
