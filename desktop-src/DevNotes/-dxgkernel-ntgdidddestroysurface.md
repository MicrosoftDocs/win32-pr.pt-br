---
description: Destrói um objeto de superfície do Microsoft DirectDraw previamente alocado no modo kernel.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Função NtGdiDdDestroySurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010187"
---
# <a name="ntgdidddestroysurface-function"></a><span data-ttu-id="25f90-103">Função NtGdiDdDestroySurface</span><span class="sxs-lookup"><span data-stu-id="25f90-103">NtGdiDdDestroySurface function</span></span>

<span data-ttu-id="25f90-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="25f90-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="25f90-105">Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="25f90-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="25f90-106">Destrói um objeto de superfície do Microsoft DirectDraw previamente alocado no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="25f90-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f90-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25f90-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a><span data-ttu-id="25f90-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25f90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f90-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25f90-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f90-110">Identificador para objeto de superfície de modo kernel alocado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="25f90-110">Handle to previously allocated kernel-mode surface object.</span></span>

</dd> <dt>

<span data-ttu-id="25f90-111">*bRealDestroy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25f90-111">*bRealDestroy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f90-112">Especifica como destruir a superfície.</span><span class="sxs-lookup"><span data-stu-id="25f90-112">Specifies how to destroy the surface.</span></span> <span data-ttu-id="25f90-113">Pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="25f90-113">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="25f90-114">TRUE</span><span class="sxs-lookup"><span data-stu-id="25f90-114">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="25f90-115">Destrua a superfície e libere memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="25f90-115">Destroy the surface and free video memory.</span></span>

</dd> <dt>



 <span data-ttu-id="25f90-116">FOR</span><span class="sxs-lookup"><span data-stu-id="25f90-116">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="25f90-117">Libere a memória de vídeo, mas deixe a superfície em um estado não inicializado.</span><span class="sxs-lookup"><span data-stu-id="25f90-117">Free the video memory but leave the surface in an uninitialized state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f90-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25f90-118">Return value</span></span>

<span data-ttu-id="25f90-119">**NtGdiDdDestroySurface** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="25f90-119">**NtGdiDdDestroySurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="25f90-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="25f90-120">Return code</span></span>                                                                                              | <span data-ttu-id="25f90-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="25f90-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25f90-122"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="25f90-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="25f90-123">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="25f90-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="25f90-124">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="25f90-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="25f90-125">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="25f90-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="25f90-126"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="25f90-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="25f90-127">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="25f90-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="25f90-128">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="25f90-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="25f90-129">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25f90-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25f90-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="25f90-130">Remarks</span></span>

<span data-ttu-id="25f90-131">É recomendável que os aplicativos usem as APIs do DirectDraw e do Direct3D para criar e destruir superfícies em vez dessa função.</span><span class="sxs-lookup"><span data-stu-id="25f90-131">It is recommended that applications use the DirectDraw and Direct3D APIs to create and destroy surfaces instead of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="25f90-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25f90-132">Requirements</span></span>



| <span data-ttu-id="25f90-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f90-133">Requirement</span></span> | <span data-ttu-id="25f90-134">Valor</span><span class="sxs-lookup"><span data-stu-id="25f90-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25f90-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25f90-135">Minimum supported client</span></span><br/> | <span data-ttu-id="25f90-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="25f90-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="25f90-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25f90-137">Minimum supported server</span></span><br/> | <span data-ttu-id="25f90-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="25f90-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="25f90-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="25f90-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f90-140"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f90-140"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f90-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="25f90-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f90-142">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="25f90-142">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




