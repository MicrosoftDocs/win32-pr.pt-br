---
description: Executa uma transferência de bloco de bits.
ms.assetid: 90cc02af-96af-4913-ae7d-62f39cd6ddd7
title: Função NtGdiDdBlt (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBlt
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 86249a8ff1069bc0875aad3fcca576ef78b9db68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089192"
---
# <a name="ntgdiddblt-function"></a><span data-ttu-id="8ab47-103">Função NtGdiDdBlt</span><span class="sxs-lookup"><span data-stu-id="8ab47-103">NtGdiDdBlt function</span></span>

<span data-ttu-id="8ab47-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8ab47-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8ab47-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="8ab47-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8ab47-106">Executa uma transferência de bloco de bits.</span><span class="sxs-lookup"><span data-stu-id="8ab47-106">Performs a bit-block transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ab47-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ab47-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdBlt(
  _In_    HANDLE      hSurfaceDest,
  _In_    HANDLE      hSurfaceSrc,
  _Inout_ PDD_BLTDATA puBltData
);
```



## <a name="parameters"></a><span data-ttu-id="8ab47-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ab47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ab47-109">*hSurfaceDest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8ab47-109">*hSurfaceDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab47-110">Manipule uma estrutura [**\_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície na qual blit.</span><span class="sxs-lookup"><span data-stu-id="8ab47-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface on which to blit.</span></span>

</dd> <dt>

<span data-ttu-id="8ab47-111">*hSurfaceSrc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8ab47-111">*hSurfaceSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab47-112">Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície de origem.</span><span class="sxs-lookup"><span data-stu-id="8ab47-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="8ab47-113">*puBltData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8ab47-113">*puBltData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ab47-114">Ponteiro para uma [**estrutura \_ BLTDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) que contém as informações necessárias para o driver executar o blit.</span><span class="sxs-lookup"><span data-stu-id="8ab47-114">Pointer to a [**DD\_BLTDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) structure that contains the information required for the driver to perform the blit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ab47-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ab47-115">Return value</span></span>

<span data-ttu-id="8ab47-116">**NtGdiDdBlt** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8ab47-116">**NtGdiDdBlt** returns one of the following callback codes.</span></span>



| <span data-ttu-id="8ab47-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8ab47-117">Return code</span></span>                                                                                              | <span data-ttu-id="8ab47-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ab47-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ab47-119"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="8ab47-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="8ab47-120">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="8ab47-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="8ab47-121">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="8ab47-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="8ab47-122">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="8ab47-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="8ab47-123"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="8ab47-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="8ab47-124">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="8ab47-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="8ab47-125">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="8ab47-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="8ab47-126">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ab47-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ab47-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ab47-127">Requirements</span></span>



| <span data-ttu-id="8ab47-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ab47-128">Requirement</span></span> | <span data-ttu-id="8ab47-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8ab47-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ab47-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ab47-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8ab47-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8ab47-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8ab47-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ab47-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8ab47-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8ab47-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ab47-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8ab47-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ab47-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ab47-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ab47-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ab47-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab47-137">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="8ab47-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
