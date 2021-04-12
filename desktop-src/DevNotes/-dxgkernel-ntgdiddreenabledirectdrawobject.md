---
description: Habilita novamente um objeto de dispositivo do modo kernel do Microsoft DirectDraw após uma opção de modo.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Função NtGdiDdReenableDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089438"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a><span data-ttu-id="89f07-103">Função NtGdiDdReenableDirectDrawObject</span><span class="sxs-lookup"><span data-stu-id="89f07-103">NtGdiDdReenableDirectDrawObject function</span></span>

<span data-ttu-id="89f07-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="89f07-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="89f07-105">Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="89f07-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="89f07-106">Habilita novamente um objeto de dispositivo do modo kernel do Microsoft DirectDraw após uma opção de modo.</span><span class="sxs-lookup"><span data-stu-id="89f07-106">Re-enables a Microsoft DirectDraw kernel-mode device object after a mode switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f07-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89f07-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a><span data-ttu-id="89f07-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89f07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f07-109">*hDirectDrawLocal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89f07-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f07-110">O objeto DirectDraw que precisa ser habilitado novamente.</span><span class="sxs-lookup"><span data-stu-id="89f07-110">DirectDraw object that needs to be re-enabled.</span></span>

</dd> <dt>

<span data-ttu-id="89f07-111">*pubNewMode* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="89f07-111">*pubNewMode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="89f07-112">Ponteiro para um BOOL que será preenchido com um valor que representa se o modo de exibição foi alterado.</span><span class="sxs-lookup"><span data-stu-id="89f07-112">Pointer to a BOOL that will be filled with a value that represents whether the display mode changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f07-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89f07-113">Return value</span></span>

<span data-ttu-id="89f07-114">Se for bem-sucedido (o dispositivo pode ser habilitado novamente), essa função retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="89f07-114">If successful (the device can be re-enabled), this function returns **TRUE**.</span></span> <span data-ttu-id="89f07-115">Caso contrário (por exemplo, o driver de vídeo foi alterado), ele retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="89f07-115">Otherwise (for example, the display driver was changed), it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89f07-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="89f07-116">Remarks</span></span>

<span data-ttu-id="89f07-117">Depois que o objeto tiver sido reabilitado, os recursos do dispositivo poderão ser consultados novamente por meio de uma chamada para [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span><span class="sxs-lookup"><span data-stu-id="89f07-117">Once the object has been re-enabled, the capabilities for the device can be re-queried via a call to [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).</span></span>

<span data-ttu-id="89f07-118">Os aplicativos são aconselhados a usar as APIs do DirectDraw ou do [Direct3D](../direct3d10/d3d10-graphics-reference.md) versão 8, que automatizam e abstraem esse processo de maneira independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="89f07-118">Applications are advised to use the DirectDraw or [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8 APIs, which automate and abstract this process in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f07-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89f07-119">Requirements</span></span>



| <span data-ttu-id="89f07-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f07-120">Requirement</span></span> | <span data-ttu-id="89f07-121">Valor</span><span class="sxs-lookup"><span data-stu-id="89f07-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89f07-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89f07-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89f07-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89f07-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="89f07-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89f07-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89f07-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89f07-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89f07-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="89f07-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="89f07-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="89f07-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89f07-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="89f07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f07-129">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="89f07-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="89f07-130">**DdReenableDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="89f07-130">**DdReenableDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
