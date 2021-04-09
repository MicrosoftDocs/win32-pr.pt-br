---
description: Consulta a quantidade de memória livre em todos os heaps de memória de vídeo.
ms.assetid: 6718e8da-0da0-42e3-a02b-6884b141fe24
title: Função NtGdiDdGetAvailDriverMemory (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetAvailDriverMemory
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c6ec322665b84b3ddad14b7032b8e49245377d40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010184"
---
# <a name="ntgdiddgetavaildrivermemory-function"></a><span data-ttu-id="e349c-103">Função NtGdiDdGetAvailDriverMemory</span><span class="sxs-lookup"><span data-stu-id="e349c-103">NtGdiDdGetAvailDriverMemory function</span></span>

<span data-ttu-id="e349c-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e349c-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e349c-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="e349c-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e349c-106">Consulta a quantidade de memória livre em todos os heaps de memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e349c-106">Queries the amount of free memory in all video memory heaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="e349c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e349c-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetAvailDriverMemory(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_GETAVAILDRIVERMEMORYDATA puGetAvailDriverMemoryData
);
```



## <a name="parameters"></a><span data-ttu-id="e349c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e349c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e349c-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e349c-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e349c-110">Identificador para objeto DirectDraw do modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e349c-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="e349c-111">*puGetAvailDriverMemoryData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e349c-111">*puGetAvailDriverMemoryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e349c-112">Ponteiro para uma [estrutura \_ GETAVAILDRIVERMEMORYDATA do DD](https://msdn.microsoft.com/library/ms794088.aspx) que contém as informações necessárias para executar a consulta.</span><span class="sxs-lookup"><span data-stu-id="e349c-112">Pointer to a [DD\_GETAVAILDRIVERMEMORYDATA](https://msdn.microsoft.com/library/ms794088.aspx) structure that contains the information required to perform the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e349c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e349c-113">Return value</span></span>

<span data-ttu-id="e349c-114">**NtGdiDdGetAvailDriverMemory** retorna um dos seguintes códigos de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e349c-114">**NtGdiDdGetAvailDriverMemory** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e349c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e349c-115">Return code</span></span>                                                                                              | <span data-ttu-id="e349c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e349c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e349c-117"><dt>**\_Driver DDHAL \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="e349c-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e349c-118">O driver executou a operação e retornou um código de retorno válido para essa operação.</span><span class="sxs-lookup"><span data-stu-id="e349c-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e349c-119">Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função.</span><span class="sxs-lookup"><span data-stu-id="e349c-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e349c-120">Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.</span><span class="sxs-lookup"><span data-stu-id="e349c-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e349c-121"><dt>**Driver DDHAL não \_ \_ manipulado**</dt></span><span class="sxs-lookup"><span data-stu-id="e349c-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e349c-122">O driver não tem nenhum comentário sobre a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="e349c-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e349c-123">Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="e349c-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e349c-124">Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e349c-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e349c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e349c-125">Requirements</span></span>



| <span data-ttu-id="e349c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e349c-126">Requirement</span></span> | <span data-ttu-id="e349c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e349c-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e349c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e349c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e349c-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e349c-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e349c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e349c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e349c-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e349c-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e349c-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e349c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e349c-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e349c-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e349c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e349c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e349c-135">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="e349c-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




