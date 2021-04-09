---
description: Renderiza primitivos e retorna o estado de renderização atualizado.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: Função NtGdiD3DDrawPrimitives2 (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010131"
---
# <a name="ntgdid3ddrawprimitives2-function"></a><span data-ttu-id="8c187-103">Função NtGdiD3DDrawPrimitives2</span><span class="sxs-lookup"><span data-stu-id="8c187-103">NtGdiD3DDrawPrimitives2 function</span></span>

<span data-ttu-id="8c187-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8c187-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8c187-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="8c187-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8c187-106">Renderiza primitivos e retorna o estado de renderização atualizado.</span><span class="sxs-lookup"><span data-stu-id="8c187-106">Renders primitives and returns the updated render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c187-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c187-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a><span data-ttu-id="8c187-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c187-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c187-109">*hCmdBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c187-109">*hCmdBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c187-110">Manipule a estrutura [**\_ \_ local da superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que identifica a superfície do DirectDraw que contém os dados do comando.</span><span class="sxs-lookup"><span data-stu-id="8c187-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the command data.</span></span>

</dd> <dt>

<span data-ttu-id="8c187-111">*hVBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c187-111">*hVBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c187-112">Manipule a estrutura [**\_ \_ local da superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que identifica a superfície do DirectDraw que contém os dados do vértice.</span><span class="sxs-lookup"><span data-stu-id="8c187-112">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the vertex data.</span></span>

</dd> <dt>

<span data-ttu-id="8c187-113">*pded* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8c187-113">*pded* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c187-114">Ponteiro para uma estrutura [**D3DNTHAL \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) que contém as informações necessárias para o driver processar um ou mais primitivos.</span><span class="sxs-lookup"><span data-stu-id="8c187-114">Pointer to a [**D3DNTHAL\_DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to render one or more primitives.</span></span>

</dd> <dt>

<span data-ttu-id="8c187-115">*pfpVidMemCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8c187-115">*pfpVidMemCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c187-116">Novo ponteiro para memória de vídeo se o driver permutau o buffer de comando.</span><span class="sxs-lookup"><span data-stu-id="8c187-116">New pointer to video memory if the driver swapped the command buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8c187-117">*pdwSizeCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8c187-117">*pdwSizeCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c187-118">Especifica o número mínimo de bytes para os quais o driver deve aumentar o buffer do comando de permuta.</span><span class="sxs-lookup"><span data-stu-id="8c187-118">Specifies the minimum number of bytes that the driver must increase the swap command buffer by.</span></span>

</dd> <dt>

<span data-ttu-id="8c187-119">*pfpVidMemVtx* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8c187-119">*pfpVidMemVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c187-120">Novo ponteiro para memória de vídeo se o driver permutau o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="8c187-120">New pointer to video memory if the driver swapped the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8c187-121">*pdwSizeVtx* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8c187-121">*pdwSizeVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c187-122">Especifica o número mínimo de bytes que o driver deve alocar para o buffer de vértice de permuta.</span><span class="sxs-lookup"><span data-stu-id="8c187-122">Specifies the minimum number of bytes that the driver must allocate for the swap vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c187-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c187-123">Return value</span></span>

<span data-ttu-id="8c187-124">**NtGdiD3DDrawPrimitives2** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8c187-124">**NtGdiD3DDrawPrimitives2** returns one of the following callback codes.</span></span>



| <span data-ttu-id="8c187-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8c187-125">Return code</span></span>                                                                                              | <span data-ttu-id="8c187-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c187-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c187-127"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="8c187-127"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="8c187-128">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="8c187-128">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="8c187-129">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="8c187-129">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="8c187-130">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="8c187-130">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="8c187-131"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="8c187-131"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="8c187-132">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="8c187-132">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="8c187-133">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="8c187-133">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="8c187-134">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8c187-134">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8c187-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c187-135">Requirements</span></span>



| <span data-ttu-id="8c187-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c187-136">Requirement</span></span> | <span data-ttu-id="8c187-137">Valor</span><span class="sxs-lookup"><span data-stu-id="8c187-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c187-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c187-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8c187-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c187-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8c187-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c187-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8c187-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c187-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8c187-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8c187-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c187-143"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c187-143"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c187-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c187-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c187-145">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="8c187-145">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
