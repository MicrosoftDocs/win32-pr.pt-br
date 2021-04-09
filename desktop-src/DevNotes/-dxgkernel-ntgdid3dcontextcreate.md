---
description: Cria um contexto.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: Função NtGdiD3DContextCreate (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: f59a80d3efd5e077bc1eadea66255ff5e6ea7523
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088926"
---
# <a name="ntgdid3dcontextcreate-function"></a><span data-ttu-id="28d4e-103">Função NtGdiD3DContextCreate</span><span class="sxs-lookup"><span data-stu-id="28d4e-103">NtGdiD3DContextCreate function</span></span>

<span data-ttu-id="28d4e-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="28d4e-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="28d4e-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="28d4e-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="28d4e-106">Cria um contexto.</span><span class="sxs-lookup"><span data-stu-id="28d4e-106">Creates a context.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d4e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28d4e-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a><span data-ttu-id="28d4e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28d4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28d4e-109">*hDirectDrawLocal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28d4e-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28d4e-110">Identificador para um objeto DirectDraw no modo kernel, criado anteriormente com [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), que representa o dispositivo no qual o contexto do Direct3D deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="28d4e-110">Handle to a kernel-mode DirectDraw object, previously created with [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representing the device on which the Direct3D context is to be created.</span></span>

</dd> <dt>

<span data-ttu-id="28d4e-111">*hSurfColor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28d4e-111">*hSurfColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28d4e-112">Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície do DirectDraw a ser usada como o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="28d4e-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as the rendering target.</span></span>

</dd> <dt>

<span data-ttu-id="28d4e-113">*hSurfZ* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28d4e-113">*hSurfZ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28d4e-114">Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície do DirectDraw a ser usada como um buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="28d4e-114">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as a depth buffer.</span></span> <span data-ttu-id="28d4e-115">Se esse membro for **nulo**, nenhum buffer de profundidade será executado.</span><span class="sxs-lookup"><span data-stu-id="28d4e-115">If this member is **NULL**, no depth buffering is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="28d4e-116">*pdcci* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="28d4e-116">*pdcci* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28d4e-117">Ponteiro para uma estrutura [**D3DNTHAL \_ CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) que contém as informações necessárias para criar um contexto e os dados que o driver deve armazenar no novo contexto.</span><span class="sxs-lookup"><span data-stu-id="28d4e-117">Pointer to a [**D3DNTHAL\_CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required to create a context and the data that the driver should store in the new context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28d4e-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28d4e-118">Return value</span></span>

<span data-ttu-id="28d4e-119">**NtGdiD3DContextCreate** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="28d4e-119">**NtGdiD3DContextCreate** returns one of the following callback codes.</span></span>



| <span data-ttu-id="28d4e-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="28d4e-120">Return code</span></span>                                                                                              | <span data-ttu-id="28d4e-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="28d4e-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28d4e-122"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="28d4e-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="28d4e-123">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="28d4e-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="28d4e-124">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="28d4e-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="28d4e-125">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="28d4e-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="28d4e-126"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="28d4e-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="28d4e-127">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="28d4e-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="28d4e-128">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="28d4e-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="28d4e-129">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28d4e-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28d4e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28d4e-130">Requirements</span></span>



| <span data-ttu-id="28d4e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d4e-131">Requirement</span></span> | <span data-ttu-id="28d4e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="28d4e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28d4e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28d4e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="28d4e-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28d4e-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="28d4e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28d4e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="28d4e-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28d4e-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="28d4e-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="28d4e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d4e-138"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d4e-138"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d4e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="28d4e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d4e-140">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="28d4e-140">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
