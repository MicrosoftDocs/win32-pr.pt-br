---
description: Consulta a quantidade de memória livre no heap de memória gerenciada por driver.
ms.assetid: d7f8792b-a515-4e70-9474-6a3474b6612b
title: Função NtGdiD3DContextDestroyAll (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroyAll
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8bb42c902555568ebe7a26656cd188e9c8e40213
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826288"
---
# <a name="ntgdid3dcontextdestroyall-function"></a><span data-ttu-id="89b54-103">Função NtGdiD3DContextDestroyAll</span><span class="sxs-lookup"><span data-stu-id="89b54-103">NtGdiD3DContextDestroyAll function</span></span>

<span data-ttu-id="89b54-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="89b54-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="89b54-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="89b54-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="89b54-106">Consulta a quantidade de memória livre no heap de memória gerenciada por driver.</span><span class="sxs-lookup"><span data-stu-id="89b54-106">Queries the amount of free memory in the driver-managed memory heap.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b54-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89b54-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroyAll(void);
```



## <a name="parameters"></a><span data-ttu-id="89b54-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89b54-108">Parameters</span></span>

<span data-ttu-id="89b54-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="89b54-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89b54-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="89b54-110">Return value</span></span>

<span data-ttu-id="89b54-111">**NtGdiD3DContextDestroyAll** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="89b54-111">**NtGdiD3DContextDestroyAll** returns one of the following callback codes.</span></span>



| <span data-ttu-id="89b54-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="89b54-112">Return code</span></span>                                                                                              | <span data-ttu-id="89b54-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="89b54-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89b54-114"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="89b54-114"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="89b54-115">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="89b54-115">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="89b54-116">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="89b54-116">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="89b54-117">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="89b54-117">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="89b54-118"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="89b54-118"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="89b54-119">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="89b54-119">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="89b54-120">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="89b54-120">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="89b54-121">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89b54-121">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="89b54-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89b54-122">Requirements</span></span>



| <span data-ttu-id="89b54-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89b54-123">Requirement</span></span> | <span data-ttu-id="89b54-124">Valor</span><span class="sxs-lookup"><span data-stu-id="89b54-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89b54-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89b54-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89b54-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89b54-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="89b54-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89b54-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89b54-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89b54-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89b54-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="89b54-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="89b54-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="89b54-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b54-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="89b54-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b54-132">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="89b54-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




