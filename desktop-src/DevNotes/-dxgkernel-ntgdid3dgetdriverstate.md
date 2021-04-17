---
description: Usado pelos tempos de execução do Microsoft DirectDraw e do Microsoft Direct3D para obter informações do driver sobre seu estado atual.
ms.assetid: a7697e0c-9485-4a9c-b211-67ce07dc3604
title: Função NtGdiD3DGetDriverState (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DGetDriverState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: c88f2fde4d848aac5ecae3c60aef77d4c6b783cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754789"
---
# <a name="ntgdid3dgetdriverstate-function"></a><span data-ttu-id="32db2-103">Função NtGdiD3DGetDriverState</span><span class="sxs-lookup"><span data-stu-id="32db2-103">NtGdiD3DGetDriverState function</span></span>

<span data-ttu-id="32db2-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="32db2-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="32db2-105">Em vez disso, use o DirectDraw e o Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="32db2-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="32db2-106">Usado pelos tempos de execução do Microsoft DirectDraw e do Microsoft Direct3D para obter informações do driver sobre seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="32db2-106">Used by both the Microsoft DirectDraw and Microsoft Direct3D runtimes to obtain information from the driver about its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="32db2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32db2-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DGetDriverState(
  _Inout_ PDD_GETDRIVERSTATEDATA pdata
);
```



## <a name="parameters"></a><span data-ttu-id="32db2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32db2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32db2-109">*pData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="32db2-109">*pdata* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32db2-110">Ponteiro para uma [**estrutura \_ GETDRIVERSTATEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) que descreve o estado do driver.</span><span class="sxs-lookup"><span data-stu-id="32db2-110">Pointer to a [**DD\_GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) structure that describes the state of the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32db2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32db2-111">Return value</span></span>

<span data-ttu-id="32db2-112">**NtGdiD3DGetDriverState** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="32db2-112">**NtGdiD3DGetDriverState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="32db2-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="32db2-113">Return code</span></span>                                                                                              | <span data-ttu-id="32db2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="32db2-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32db2-115"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="32db2-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="32db2-116">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="32db2-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="32db2-117">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="32db2-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="32db2-118">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="32db2-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="32db2-119"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="32db2-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="32db2-120">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="32db2-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="32db2-121">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="32db2-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="32db2-122">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32db2-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="32db2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32db2-123">Requirements</span></span>



| <span data-ttu-id="32db2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="32db2-124">Requirement</span></span> | <span data-ttu-id="32db2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="32db2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32db2-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32db2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="32db2-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="32db2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="32db2-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32db2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="32db2-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="32db2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="32db2-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="32db2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="32db2-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="32db2-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32db2-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="32db2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32db2-133">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="32db2-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
