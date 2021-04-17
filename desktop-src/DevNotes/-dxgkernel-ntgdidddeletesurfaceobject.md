---
description: NtGdiDdDeleteSurfaceObject exclui um objeto de superfície de modo de kernel criado anteriormente.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: Função NtGdiDdDeleteSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03988b842aacc29915287490508eb9e9d057e907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749291"
---
# <a name="ntgdidddeletesurfaceobject-function"></a><span data-ttu-id="b0074-103">Função NtGdiDdDeleteSurfaceObject</span><span class="sxs-lookup"><span data-stu-id="b0074-103">NtGdiDdDeleteSurfaceObject function</span></span>

<span data-ttu-id="b0074-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b0074-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b0074-105">Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="b0074-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b0074-106">**NtGdiDdDeleteSurfaceObject** exclui um objeto de superfície de modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b0074-106">**NtGdiDdDeleteSurfaceObject** deletes a previously created kernel-mode surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0074-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0074-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="b0074-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0074-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0074-109">*hSurface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0074-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0074-110">Identificador para o objeto de superfície do modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b0074-110">Handle to the previously created kernel-mode surface object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0074-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0074-111">Return value</span></span>

<span data-ttu-id="b0074-112">Se for bem-sucedida, essa função retornará **true**; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="b0074-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0074-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0074-113">Remarks</span></span>

<span data-ttu-id="b0074-114">Os aplicativos são aconselhados a usar as APIs do DirectDraw e do [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="b0074-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="b0074-115">Essas construções abstraem o processo de criação de dispositivos de maneira simplificada e independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b0074-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0074-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0074-116">Requirements</span></span>



| <span data-ttu-id="b0074-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0074-117">Requirement</span></span> | <span data-ttu-id="b0074-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b0074-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0074-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0074-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0074-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0074-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b0074-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0074-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0074-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0074-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b0074-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b0074-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0074-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0074-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0074-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0074-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0074-126">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="b0074-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="b0074-127">**DdDeleteSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="b0074-127">**DdDeleteSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[<span data-ttu-id="b0074-128">**NtGdiDdCreateSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="b0074-128">**NtGdiDdCreateSurfaceObject**</span></span>](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
