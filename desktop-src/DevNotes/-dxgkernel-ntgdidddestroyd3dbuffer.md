---
description: Destrói um objeto de superfície do Microsoft DirectDraw do modo de kernel alocado anteriormente que foi criado com o membro dwCaps da estrutura DDSCAPS definida como DDSCAPS \_ EXECUTEBUFFER.
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: Função NtGdiDdDestroyD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: e88394e8cc3d13e1d117a1e53eab1190b1290ca4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646204"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a><span data-ttu-id="b868c-103">Função NtGdiDdDestroyD3DBuffer</span><span class="sxs-lookup"><span data-stu-id="b868c-103">NtGdiDdDestroyD3DBuffer function</span></span>

<span data-ttu-id="b868c-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b868c-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b868c-105">Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="b868c-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b868c-106">Destrói um objeto de superfície do Microsoft DirectDraw do modo de kernel alocado anteriormente que foi criado com o membro **dwCaps** da estrutura [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) definida como DDSCAPS \_ EXECUTEBUFFER.</span><span class="sxs-lookup"><span data-stu-id="b868c-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object that was created with the **dwCaps** member of the [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) structure set to DDSCAPS\_EXECUTEBUFFER.</span></span>

## <a name="syntax"></a><span data-ttu-id="b868c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b868c-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="b868c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b868c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b868c-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b868c-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b868c-110">Identificador para uma [**estrutura \_ DESTROYSURFACEDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) que contém as informações necessárias para destruir um comando do Direct3D ou um buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="b868c-110">Handle to a [**DD\_DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) structure that contains the information needed to destroy a Direct3D command or vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b868c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b868c-111">Return value</span></span>

<span data-ttu-id="b868c-112">**NtGdiDdDestroyD3DBuffer** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b868c-112">**NtGdiDdDestroyD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="b868c-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b868c-113">Return code</span></span>                                                                                              | <span data-ttu-id="b868c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b868c-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b868c-115"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="b868c-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="b868c-116">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="b868c-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="b868c-117">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="b868c-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="b868c-118">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="b868c-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b868c-119"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="b868c-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="b868c-120">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="b868c-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="b868c-121">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="b868c-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="b868c-122">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b868c-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b868c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b868c-123">Requirements</span></span>



| <span data-ttu-id="b868c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b868c-124">Requirement</span></span> | <span data-ttu-id="b868c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b868c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b868c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b868c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b868c-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b868c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b868c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b868c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b868c-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b868c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b868c-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b868c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b868c-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b868c-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b868c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b868c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b868c-133">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="b868c-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
