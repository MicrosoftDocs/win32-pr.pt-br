---
description: Define o valor da chave de cor para a superfície especificada.
ms.assetid: 052dba97-c047-4ef7-a908-2a66ade3af10
title: Função NtGdiDdSetColorKey (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetColorKey
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7d6186df13ee88ca3de4f123381c012548b1cd85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500788"
---
# <a name="ntgdiddsetcolorkey-function"></a><span data-ttu-id="218b1-103">Função NtGdiDdSetColorKey</span><span class="sxs-lookup"><span data-stu-id="218b1-103">NtGdiDdSetColorKey function</span></span>

<span data-ttu-id="218b1-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="218b1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="218b1-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="218b1-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="218b1-106">Define o valor da chave de cor para a superfície especificada.</span><span class="sxs-lookup"><span data-stu-id="218b1-106">Sets the color key value for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="218b1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="218b1-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetColorKey(
  _In_    HANDLE              hSurface,
  _Inout_ PDD_SETCOLORKEYDATA puSetColorKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="218b1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="218b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="218b1-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="218b1-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218b1-110">Ponteiro para a [**estrutura \_ \_ local da superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície com a qual a chave de cor deve ser associada.</span><span class="sxs-lookup"><span data-stu-id="218b1-110">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface with which the color key is to be associated.</span></span>

</dd> <dt>

<span data-ttu-id="218b1-111">*puSetColorKeyData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="218b1-111">*puSetColorKeyData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="218b1-112">Ponteiro para uma [**estrutura \_ SETCOLORKEYDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) que contém as informações necessárias para definir a chave de cor para a superfície especificada.</span><span class="sxs-lookup"><span data-stu-id="218b1-112">Pointer to a [**DD\_SETCOLORKEYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setcolorkeydata) structure that contains the information required to set the color key for the specified surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="218b1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="218b1-113">Return value</span></span>

<span data-ttu-id="218b1-114">**NtGdiDdSetColorKey** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="218b1-114">**NtGdiDdSetColorKey** returns one of the following callback codes.</span></span>



| <span data-ttu-id="218b1-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="218b1-115">Return code</span></span>                                                                                              | <span data-ttu-id="218b1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="218b1-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="218b1-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="218b1-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="218b1-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="218b1-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="218b1-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="218b1-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="218b1-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="218b1-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="218b1-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="218b1-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="218b1-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="218b1-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="218b1-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="218b1-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="218b1-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="218b1-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="218b1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="218b1-125">Requirements</span></span>



| <span data-ttu-id="218b1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="218b1-126">Requirement</span></span> | <span data-ttu-id="218b1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="218b1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="218b1-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="218b1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="218b1-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="218b1-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="218b1-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="218b1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="218b1-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="218b1-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="218b1-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="218b1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="218b1-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="218b1-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="218b1-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="218b1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="218b1-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="218b1-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
