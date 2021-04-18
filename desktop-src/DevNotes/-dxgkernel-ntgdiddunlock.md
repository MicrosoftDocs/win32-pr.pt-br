---
description: Libera o bloqueio mantido na superfície especificada.
ms.assetid: d9d3178b-aadd-4c33-8044-8e6362f9fefe
title: Função NtGdiDdUnlock (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnlock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3472dc32cc503b83c12bcc17cdbd0d14b89b0de4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456912"
---
# <a name="ntgdiddunlock-function"></a><span data-ttu-id="6d645-103">Função NtGdiDdUnlock</span><span class="sxs-lookup"><span data-stu-id="6d645-103">NtGdiDdUnlock function</span></span>

<span data-ttu-id="6d645-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6d645-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="6d645-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="6d645-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="6d645-106">Libera o bloqueio mantido na superfície especificada.</span><span class="sxs-lookup"><span data-stu-id="6d645-106">Releases the lock held on the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d645-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d645-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUnlock(
  _In_    HANDLE         hSurface,
  _Inout_ PDD_UNLOCKDATA puUnlockData
);
```



## <a name="parameters"></a><span data-ttu-id="6d645-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d645-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d645-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d645-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d645-110">Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície a ser desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="6d645-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface to be unlocked.</span></span>

</dd> <dt>

<span data-ttu-id="6d645-111">*puUnlockData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6d645-111">*puUnlockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d645-112">Ponteiro para uma [**estrutura \_ UNLOCKDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) que contém as informações necessárias para executar a liberação de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="6d645-112">Pointer to a [**DD\_UNLOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) structure that contains the information required to perform the lock release.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d645-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d645-113">Return value</span></span>

<span data-ttu-id="6d645-114">**NtGdiDdUnlock** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6d645-114">**NtGdiDdUnlock** returns one of the following callback codes.</span></span>



| <span data-ttu-id="6d645-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6d645-115">Return code</span></span>                                                                                              | <span data-ttu-id="6d645-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d645-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d645-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="6d645-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="6d645-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="6d645-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="6d645-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="6d645-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="6d645-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="6d645-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="6d645-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="6d645-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="6d645-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="6d645-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="6d645-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="6d645-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="6d645-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d645-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6d645-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d645-125">Requirements</span></span>



| <span data-ttu-id="6d645-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d645-126">Requirement</span></span> | <span data-ttu-id="6d645-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6d645-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d645-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d645-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6d645-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d645-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6d645-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d645-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6d645-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d645-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d645-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6d645-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d645-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d645-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d645-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d645-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d645-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="6d645-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
