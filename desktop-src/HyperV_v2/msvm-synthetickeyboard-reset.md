---
description: Redefine o teclado virtual.
ms.assetid: 2a943dd8-3b94-4b20-8786-7f9d8b0aeaa6
title: Método Reset da classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 05c5b8dbfba04eca6e0b118ae20f2ad172d324e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164295"
---
# <a name="reset-method-of-the-msvm_synthetickeyboard-class"></a><span data-ttu-id="ffa89-103">Método Reset da classe Msvm \_ SyntheticKeyboard</span><span class="sxs-lookup"><span data-stu-id="ffa89-103">Reset method of the Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="ffa89-104">Redefine o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="ffa89-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffa89-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="ffa89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffa89-106">Parameters</span></span>

<span data-ttu-id="ffa89-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ffa89-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ffa89-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ffa89-108">Return value</span></span>

<span data-ttu-id="ffa89-109">Em caso de sucesso, retorna 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ffa89-109">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ffa89-110">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="ffa89-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ffa89-111">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="ffa89-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ffa89-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffa89-112">Requirements</span></span>



| <span data-ttu-id="ffa89-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffa89-113">Requirement</span></span> | <span data-ttu-id="ffa89-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ffa89-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa89-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffa89-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa89-116">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ffa89-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ffa89-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffa89-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa89-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ffa89-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ffa89-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffa89-119">Namespace</span></span><br/>                | <span data-ttu-id="ffa89-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ffa89-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffa89-121">MOF</span><span class="sxs-lookup"><span data-stu-id="ffa89-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffa89-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffa89-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffa89-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ffa89-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffa89-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffa89-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffa89-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffa89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa89-126">**Msvm \_ SyntheticKeyboard**</span><span class="sxs-lookup"><span data-stu-id="ffa89-126">**Msvm\_SyntheticKeyboard**</span></span>](msvm-synthetickeyboard.md)
</dt> </dl>

 

 




