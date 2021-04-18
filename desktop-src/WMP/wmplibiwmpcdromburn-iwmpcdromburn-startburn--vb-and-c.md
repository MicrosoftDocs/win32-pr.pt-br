---
title: Método IWMPCdromBurn startBurn
description: O método startBurn grava o CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- método startBurn Windows Media Player
- método startBurn Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, método startBurn
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787675"
---
# <a name="iwmpcdromburnstartburn-method"></a><span data-ttu-id="e49a5-106">Método IWMPCdromBurn:: startBurn</span><span class="sxs-lookup"><span data-stu-id="e49a5-106">IWMPCdromBurn::startBurn method</span></span>

<span data-ttu-id="e49a5-107">O método **startBurn** grava o CD.</span><span class="sxs-lookup"><span data-stu-id="e49a5-107">The **startBurn** method burns the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="e49a5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e49a5-108">Syntax</span></span>


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a><span data-ttu-id="e49a5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e49a5-109">Parameters</span></span>

<span data-ttu-id="e49a5-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e49a5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e49a5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e49a5-111">Return value</span></span>

<span data-ttu-id="e49a5-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e49a5-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e49a5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e49a5-113">Remarks</span></span>

<span data-ttu-id="e49a5-114">O valor de **burnstate** deve ser WmpbsReady ou wmpbsStopped antes de chamar este método.</span><span class="sxs-lookup"><span data-stu-id="e49a5-114">The value of **burnstate** should be wmpbsReady or wmpbsStopped before calling this method.</span></span>

<span data-ttu-id="e49a5-115">Esse método não funcionará se a unidade de CD não for um gravador ou se o disco na unidade não for gravável.</span><span class="sxs-lookup"><span data-stu-id="e49a5-115">This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable.</span></span> <span data-ttu-id="e49a5-116">Use **IsAvailable** para determinar se um CD pode ser gravado.</span><span class="sxs-lookup"><span data-stu-id="e49a5-116">Use **isAvailable** to determine whether a CD can be burned.</span></span>

## <a name="requirements"></a><span data-ttu-id="e49a5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e49a5-117">Requirements</span></span>



| <span data-ttu-id="e49a5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e49a5-118">Requirement</span></span> | <span data-ttu-id="e49a5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e49a5-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e49a5-120">Versão</span><span class="sxs-lookup"><span data-stu-id="e49a5-120">Version</span></span><br/>   | <span data-ttu-id="e49a5-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="e49a5-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="e49a5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="e49a5-122">Namespace</span></span><br/> | <span data-ttu-id="e49a5-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e49a5-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e49a5-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="e49a5-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e49a5-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e49a5-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e49a5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e49a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e49a5-127">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e49a5-127">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e49a5-128">**IWMPCdromBurn. burnstate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e49a5-128">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e49a5-129">**IWMPCdromBurn. IsAvailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e49a5-129">**IWMPCdromBurn.isAvailable (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e49a5-130">**IWMPCdromBurn. stopBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e49a5-130">**IWMPCdromBurn.stopBurn (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





