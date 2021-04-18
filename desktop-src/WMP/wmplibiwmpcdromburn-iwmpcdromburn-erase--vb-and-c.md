---
title: Método de apagamento IWMPCdromBurn
description: O método Erase apaga o CD atual.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- método Erase Windows Media Player
- método Erase Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, método Erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788657"
---
# <a name="iwmpcdromburnerase-method"></a><span data-ttu-id="1dc1a-106">Método IWMPCdromBurn:: Erase</span><span class="sxs-lookup"><span data-stu-id="1dc1a-106">IWMPCdromBurn::erase method</span></span>

<span data-ttu-id="1dc1a-107">O método **Erase** apaga o CD atual.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-107">The **erase** method erases the current CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc1a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1dc1a-108">Syntax</span></span>


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a><span data-ttu-id="1dc1a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dc1a-109">Parameters</span></span>

<span data-ttu-id="1dc1a-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1dc1a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1dc1a-111">Return value</span></span>

<span data-ttu-id="1dc1a-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dc1a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dc1a-113">Remarks</span></span>

<span data-ttu-id="1dc1a-114">Esse método não funcionará se o disco na unidade não for regravável.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-114">This method will not work if the disc in the drive is not rewritable.</span></span> <span data-ttu-id="1dc1a-115">Use [IWMPCdromBurn. IsAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) para determinar se um CD pode ser apagado.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-115">Use [IWMPCdromBurn.isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) to determine whether a CD can be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dc1a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dc1a-116">Requirements</span></span>



| <span data-ttu-id="1dc1a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc1a-117">Requirement</span></span> | <span data-ttu-id="1dc1a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc1a-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc1a-119">Versão</span><span class="sxs-lookup"><span data-stu-id="1dc1a-119">Version</span></span><br/>   | <span data-ttu-id="1dc1a-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="1dc1a-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="1dc1a-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="1dc1a-121">Namespace</span></span><br/> | <span data-ttu-id="1dc1a-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1dc1a-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1dc1a-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="1dc1a-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1dc1a-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1dc1a-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc1a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dc1a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc1a-126">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1dc1a-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





