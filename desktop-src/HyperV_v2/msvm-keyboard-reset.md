---
description: Redefine o teclado virtual.
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Método Reset da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4fe46657177789e49b49ec2c36f0e7a9dc95394f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780974"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="1ecfb-103">Método Reset da classe de \_ teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="1ecfb-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="1ecfb-104">Redefine o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="1ecfb-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ecfb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ecfb-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="1ecfb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ecfb-106">Parameters</span></span>

<span data-ttu-id="1ecfb-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1ecfb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ecfb-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ecfb-108">Return value</span></span>

<span data-ttu-id="1ecfb-109">Um valor de retorno igual A zero indica êxito.</span><span class="sxs-lookup"><span data-stu-id="1ecfb-109">A return value of zero indicates success.</span></span> <span data-ttu-id="1ecfb-110">Um valor de retorno de um indica uma falha porque o método não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="1ecfb-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="1ecfb-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="1ecfb-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ecfb-112">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="1ecfb-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1ecfb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ecfb-113">Requirements</span></span>



| <span data-ttu-id="1ecfb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ecfb-114">Requirement</span></span> | <span data-ttu-id="1ecfb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1ecfb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecfb-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ecfb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1ecfb-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ecfb-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1ecfb-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ecfb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1ecfb-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="1ecfb-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1ecfb-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ecfb-120">Namespace</span></span><br/>                | <span data-ttu-id="1ecfb-121">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1ecfb-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ecfb-122">MOF</span><span class="sxs-lookup"><span data-stu-id="1ecfb-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ecfb-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ecfb-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ecfb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1ecfb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ecfb-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ecfb-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ecfb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ecfb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ecfb-127">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="1ecfb-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




