---
description: Retorna o número da linha de varredura física atual.
ms.assetid: 159d5ea0-25b8-4c2d-9cd4-cf4ee0ca0561
title: Função NtGdiDdGetScanLine (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetScanLine
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 814063208e8115c5ba2a7fe427e21223ac478f57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749290"
---
# <a name="ntgdiddgetscanline-function"></a><span data-ttu-id="8872f-103">Função NtGdiDdGetScanLine</span><span class="sxs-lookup"><span data-stu-id="8872f-103">NtGdiDdGetScanLine function</span></span>

<span data-ttu-id="8872f-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8872f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8872f-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="8872f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8872f-106">Retorna o número da linha de varredura física atual.</span><span class="sxs-lookup"><span data-stu-id="8872f-106">Returns the number of the current physical scan line.</span></span>

## <a name="syntax"></a><span data-ttu-id="8872f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8872f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetScanLine(
  _In_    HANDLE              hDirectDraw,
  _Inout_ PDD_GETSCANLINEDATA puGetScanLineData
);
```



## <a name="parameters"></a><span data-ttu-id="8872f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8872f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8872f-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8872f-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8872f-110">Identificador para uma [**estrutura \_ \_ global do DIRECTDRAW do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa o driver.</span><span class="sxs-lookup"><span data-stu-id="8872f-110">Handle to a [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure that represents the driver.</span></span>

</dd> <dt>

<span data-ttu-id="8872f-111">*puGetScanLineData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8872f-111">*puGetScanLineData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8872f-112">Ponteiro para uma [**estrutura \_ GETSCANLINEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getscanlinedata) na qual o driver retorna o número da linha de exame atual.</span><span class="sxs-lookup"><span data-stu-id="8872f-112">Pointer to a [**DD\_GETSCANLINEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getscanlinedata) structure in which the driver returns the number of the current scan line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8872f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8872f-113">Return value</span></span>

<span data-ttu-id="8872f-114">**NtGdiDdGetScanLine** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8872f-114">**NtGdiDdGetScanLine** returns one of the following callback codes.</span></span>



| <span data-ttu-id="8872f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8872f-115">Return code</span></span>                                                                                              | <span data-ttu-id="8872f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8872f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8872f-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="8872f-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="8872f-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="8872f-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="8872f-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="8872f-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="8872f-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="8872f-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="8872f-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="8872f-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="8872f-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="8872f-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="8872f-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="8872f-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="8872f-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8872f-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8872f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8872f-125">Requirements</span></span>



| <span data-ttu-id="8872f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8872f-126">Requirement</span></span> | <span data-ttu-id="8872f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8872f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8872f-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8872f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8872f-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8872f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8872f-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8872f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8872f-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8872f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8872f-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8872f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8872f-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8872f-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8872f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8872f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8872f-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="8872f-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
