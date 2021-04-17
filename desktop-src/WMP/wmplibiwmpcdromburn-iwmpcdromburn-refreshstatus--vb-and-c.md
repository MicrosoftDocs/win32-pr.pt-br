---
title: Método IWMPCdromBurn refreshStatus
description: O método refreshStatus atualiza as informações de status para a lista de reprodução de gravação atual.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- método refreshStatus Windows Media Player
- método refreshStatus Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, método refreshStatus
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812293"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a><span data-ttu-id="f781b-106">Método IWMPCdromBurn:: refreshStatus</span><span class="sxs-lookup"><span data-stu-id="f781b-106">IWMPCdromBurn::refreshStatus method</span></span>

<span data-ttu-id="f781b-107">O método **refreshStatus** atualiza as informações de status para a lista de reprodução de gravação atual.</span><span class="sxs-lookup"><span data-stu-id="f781b-107">The **refreshStatus** method updates the status information for the current burn playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="f781b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f781b-108">Syntax</span></span>


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a><span data-ttu-id="f781b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f781b-109">Parameters</span></span>

<span data-ttu-id="f781b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f781b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f781b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f781b-111">Return value</span></span>

<span data-ttu-id="f781b-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f781b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f781b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f781b-113">Remarks</span></span>

<span data-ttu-id="f781b-114">Você deve chamar esse método depois de criar ou alterar uma lista de reprodução de gravação antes de ler as informações de status ou gravar o CD.</span><span class="sxs-lookup"><span data-stu-id="f781b-114">You should call this method after you create or change a burn playlist before reading status information or burning the CD.</span></span> <span data-ttu-id="f781b-115">Você pode testar se uma atualização é necessária obtendo o valor de **burnstate** e verificando wmpbsRefreshStatusPending.</span><span class="sxs-lookup"><span data-stu-id="f781b-115">You can test whether a refresh is required by getting the value of **burnState** and checking for wmpbsRefreshStatusPending.</span></span>

<span data-ttu-id="f781b-116">A atualização do status é uma operação síncrona.</span><span class="sxs-lookup"><span data-stu-id="f781b-116">Refreshing the status is a synchronous operation.</span></span> <span data-ttu-id="f781b-117">Isso significa que um longo período de tempo pode decorrer antes que esse método retorne se a lista de reprodução de gravação atual for grande e contiver muitas alterações.</span><span class="sxs-lookup"><span data-stu-id="f781b-117">This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f781b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f781b-118">Requirements</span></span>



| <span data-ttu-id="f781b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f781b-119">Requirement</span></span> | <span data-ttu-id="f781b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f781b-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f781b-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f781b-121">Version</span></span><br/>   | <span data-ttu-id="f781b-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f781b-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="f781b-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f781b-123">Namespace</span></span><br/> | <span data-ttu-id="f781b-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f781b-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f781b-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="f781b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f781b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f781b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f781b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f781b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f781b-128">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f781b-128">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f781b-129">**IWMPCdromBurn. burnstate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f781b-129">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f781b-130">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="f781b-130">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





