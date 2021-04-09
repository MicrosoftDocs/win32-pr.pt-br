---
description: Define a rampa de gama para o dispositivo.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Função NtGdiDdSetGammaRamp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088915"
---
# <a name="ntgdiddsetgammaramp-function"></a><span data-ttu-id="264ba-103">Função NtGdiDdSetGammaRamp</span><span class="sxs-lookup"><span data-stu-id="264ba-103">NtGdiDdSetGammaRamp function</span></span>

<span data-ttu-id="264ba-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="264ba-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="264ba-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="264ba-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="264ba-106">Define a rampa de gama para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="264ba-106">Sets the gamma ramp for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="264ba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="264ba-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a><span data-ttu-id="264ba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="264ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="264ba-109">*hDirectDraw* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="264ba-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="264ba-110">Identificador para o objeto de driver de modo kernel para o qual a rampa deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="264ba-110">Handle to the kernel-mode driver object for which the ramp is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="264ba-111">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="264ba-111">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="264ba-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="264ba-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="264ba-113">*lpGammaRamp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="264ba-113">*lpGammaRamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="264ba-114">Ponteiro para uma matriz de estruturas **DDGAMMARAMP** .</span><span class="sxs-lookup"><span data-stu-id="264ba-114">Pointer to an array of **DDGAMMARAMP** structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="264ba-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="264ba-115">Return value</span></span>

<span data-ttu-id="264ba-116">O valor de retorno será **true** se a função for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="264ba-116">The return value is **TRUE** if the function is successful.</span></span> <span data-ttu-id="264ba-117">Caso contrário, será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="264ba-117">Otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="264ba-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="264ba-118">Remarks</span></span>

<span data-ttu-id="264ba-119">Recomenda-se que os aplicativos usem os métodos **IDirectDrawGammaControl:: SetGammaRamp** ou [**IDirect3DDevice9:: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) , pois esses métodos oferecem a mesma funcionalidade independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="264ba-119">It is recommended that applications use the **IDirectDrawGammaControl::SetGammaRamp** or [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) methods instead because these methods offer the same functionality independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="264ba-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="264ba-120">Requirements</span></span>



| <span data-ttu-id="264ba-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="264ba-121">Requirement</span></span> | <span data-ttu-id="264ba-122">Valor</span><span class="sxs-lookup"><span data-stu-id="264ba-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="264ba-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="264ba-123">Minimum supported client</span></span><br/> | <span data-ttu-id="264ba-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="264ba-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="264ba-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="264ba-125">Minimum supported server</span></span><br/> | <span data-ttu-id="264ba-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="264ba-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="264ba-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="264ba-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="264ba-128"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="264ba-128"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="264ba-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="264ba-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="264ba-130">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="264ba-130">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
