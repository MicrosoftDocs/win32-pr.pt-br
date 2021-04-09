---
description: Destrói um objeto de dispositivo do Microsoft DirectDraw no modo de kernel criado anteriormente.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Função NtGdiDdDeleteDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088917"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a><span data-ttu-id="55086-103">Função NtGdiDdDeleteDirectDrawObject</span><span class="sxs-lookup"><span data-stu-id="55086-103">NtGdiDdDeleteDirectDrawObject function</span></span>

<span data-ttu-id="55086-104">\[Essa função está sujeita a alterações em cada revisão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="55086-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="55086-105">Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="55086-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="55086-106">Destrói um objeto de dispositivo do Microsoft DirectDraw no modo de kernel criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="55086-106">Destroys a previously created kernel-mode Microsoft DirectDraw device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="55086-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55086-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a><span data-ttu-id="55086-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55086-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55086-109">*hDirectDrawLocal*</span><span class="sxs-lookup"><span data-stu-id="55086-109">*hDirectDrawLocal*</span></span> 
</dt> <dd>

<span data-ttu-id="55086-110">Identificador para o objeto de dispositivo do DirectDraw no modo kernel.</span><span class="sxs-lookup"><span data-stu-id="55086-110">Handle to the kernel-mode DirectDraw device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55086-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55086-111">Return value</span></span>

<span data-ttu-id="55086-112">Se for bem-sucedida, essa função retornará **true**; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="55086-112">If successful, this function returns **TRUE**; otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55086-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="55086-113">Remarks</span></span>

<span data-ttu-id="55086-114">Os aplicativos são aconselhados a usar as APIs do DirectDraw e do [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="55086-114">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="55086-115">Essas construções abstraem o processo de criação de dispositivos de maneira simplificada e independente do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="55086-115">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="55086-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55086-116">Requirements</span></span>



| <span data-ttu-id="55086-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="55086-117">Requirement</span></span> | <span data-ttu-id="55086-118">Valor</span><span class="sxs-lookup"><span data-stu-id="55086-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55086-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55086-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55086-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55086-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="55086-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55086-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55086-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55086-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="55086-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="55086-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55086-124"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="55086-124"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55086-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="55086-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55086-126">Suporte ao cliente de nível baixo de gráficos</span><span class="sxs-lookup"><span data-stu-id="55086-126">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="55086-127">**NtGdiDdCreateDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="55086-127">**NtGdiDdCreateDirectDrawObject**</span></span>](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[<span data-ttu-id="55086-128">**DdDeleteDirectDrawObject**</span><span class="sxs-lookup"><span data-stu-id="55086-128">**DdDeleteDirectDrawObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
