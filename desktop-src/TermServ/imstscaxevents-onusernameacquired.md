---
title: Método IMsTscAxEvents OnUserNameAcquired
description: Chamado quando o nome de usuário foi adquirido pelo controle.
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnUserNameAcquired
- Método OnUserNameAcquired Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnUserNameAcquired
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5d77f0eb739daa54f8385112b79f67f279eae9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810435"
---
# <a name="imstscaxeventsonusernameacquired-method"></a><span data-ttu-id="a53f8-106">Método IMsTscAxEvents:: OnUserNameAcquired</span><span class="sxs-lookup"><span data-stu-id="a53f8-106">IMsTscAxEvents::OnUserNameAcquired method</span></span>

<span data-ttu-id="a53f8-107">Chamado quando o nome de usuário foi adquirido pelo controle.</span><span class="sxs-lookup"><span data-stu-id="a53f8-107">Called when the user name has been acquired by the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53f8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a53f8-108">Syntax</span></span>


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a><span data-ttu-id="a53f8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a53f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a53f8-110">*bstrUserName*</span><span class="sxs-lookup"><span data-stu-id="a53f8-110">*bstrUserName*</span></span> 
</dt> <dd>

<span data-ttu-id="a53f8-111">O nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="a53f8-111">The user name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a53f8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a53f8-112">Return value</span></span>

<span data-ttu-id="a53f8-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a53f8-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a53f8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a53f8-114">Requirements</span></span>



| <span data-ttu-id="a53f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a53f8-115">Requirement</span></span> | <span data-ttu-id="a53f8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a53f8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a53f8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a53f8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a53f8-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a53f8-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a53f8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a53f8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a53f8-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a53f8-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a53f8-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a53f8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a53f8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a53f8-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a53f8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a53f8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a53f8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a53f8-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a53f8-125">IID</span><span class="sxs-lookup"><span data-stu-id="a53f8-125">IID</span></span><br/>                      | <span data-ttu-id="a53f8-126">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="a53f8-126">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a53f8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a53f8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53f8-128">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="a53f8-128">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





