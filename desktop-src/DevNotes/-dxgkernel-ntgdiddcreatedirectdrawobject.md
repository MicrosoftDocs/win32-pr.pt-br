---
description: Cria uma representação no lado do kernel do objeto Microsoft DirectDraw.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Função NtGdiDdCreateDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088919"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a><span data-ttu-id="d446a-103">Função NtGdiDdCreateDirectDrawObject</span><span class="sxs-lookup"><span data-stu-id="d446a-103">NtGdiDdCreateDirectDrawObject function</span></span>

<span data-ttu-id="d446a-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d446a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d446a-105">Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="d446a-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d446a-106">Cria uma representação no lado do kernel do objeto Microsoft DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="d446a-106">Creates a kernel-side representation of the Microsoft DirectDraw object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d446a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d446a-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a><span data-ttu-id="d446a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d446a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d446a-109">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d446a-109">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d446a-110">Qualquer dispositivo de vídeo de DC para o qual o objeto do DirectDraw deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="d446a-110">Any DC display device for which the DirectDraw object should be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d446a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d446a-111">Return value</span></span>

<span data-ttu-id="d446a-112">Se for bem-sucedida, essa função retornará um identificador para a representação de objeto do modo kernel; caso contrário, ele retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d446a-112">If successful, this function returns a handle to the kernel-mode object representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d446a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d446a-113">Remarks</span></span>

<span data-ttu-id="d446a-114">Os aplicativos são aconselhados a usar as APIs do DirectDraw e do [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="d446a-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="d446a-115">Essas construções abstraem o processo de criação de dispositivos de maneira simplificada e independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d446a-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="d446a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d446a-116">Requirements</span></span>



| <span data-ttu-id="d446a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d446a-117">Requirement</span></span> | <span data-ttu-id="d446a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d446a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d446a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d446a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d446a-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d446a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d446a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d446a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d446a-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d446a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d446a-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d446a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d446a-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d446a-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d446a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d446a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d446a-126">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="d446a-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="d446a-127">**DdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="d446a-127">**DdCreateDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
