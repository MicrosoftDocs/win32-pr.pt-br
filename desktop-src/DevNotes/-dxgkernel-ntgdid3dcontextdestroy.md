---
description: Exclui o contexto especificado.
ms.assetid: ac113178-bdb6-4601-940d-6b00b339904d
title: Função NtGdiD3DContextDestroy (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroy
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 19799c3895072011dd104deec18664d1ffc52b9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500946"
---
# <a name="ntgdid3dcontextdestroy-function"></a><span data-ttu-id="2f213-103">Função NtGdiD3DContextDestroy</span><span class="sxs-lookup"><span data-stu-id="2f213-103">NtGdiD3DContextDestroy function</span></span>

<span data-ttu-id="2f213-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2f213-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="2f213-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="2f213-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="2f213-106">Exclui o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="2f213-106">Deletes the specified context.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f213-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f213-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroy(
  _In_ LPD3DNTHAL_CONTEXTDESTROYDATA pContextDestroyData
);
```



## <a name="parameters"></a><span data-ttu-id="2f213-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f213-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f213-109">*pContextDestroyData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f213-109">*pContextDestroyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f213-110">Ponteiro para uma estrutura [**D3DNTHAL \_ CONTEXTDESTROYDATA**](/windows-hardware/drivers/ddi/) que contém as informações necessárias para que o driver destrua o contexto.</span><span class="sxs-lookup"><span data-stu-id="2f213-110">Pointer to a [**D3DNTHAL\_CONTEXTDESTROYDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to destroy the context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f213-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f213-111">Return value</span></span>

<span data-ttu-id="2f213-112">**NtGdiD3DContextDestroy** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="2f213-112">**NtGdiD3DContextDestroy** returns one of the following callback codes.</span></span>



| <span data-ttu-id="2f213-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2f213-113">Return code</span></span>                                                                                              | <span data-ttu-id="2f213-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f213-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f213-115"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="2f213-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="2f213-116">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="2f213-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="2f213-117">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="2f213-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="2f213-118">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="2f213-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="2f213-119"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="2f213-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="2f213-120">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="2f213-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="2f213-121">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="2f213-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="2f213-122">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f213-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2f213-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f213-123">Requirements</span></span>



| <span data-ttu-id="2f213-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f213-124">Requirement</span></span> | <span data-ttu-id="2f213-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2f213-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f213-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f213-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2f213-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f213-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2f213-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f213-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2f213-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f213-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f213-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2f213-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f213-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f213-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f213-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f213-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f213-133">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="2f213-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
