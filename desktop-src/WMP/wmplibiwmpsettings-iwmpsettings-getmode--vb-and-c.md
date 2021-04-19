---
title: Método GetMode IWMPSettings
description: O método GetMode retorna um valor que indica se o modo de loop ou o modo de ordem aleatória está ativo.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- método GetMode do Windows Media Player
- método GetMode Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, método GetMode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814446"
---
# <a name="iwmpsettingsgetmode-method"></a><span data-ttu-id="67acf-106">Método IWMPSettings:: GetMode</span><span class="sxs-lookup"><span data-stu-id="67acf-106">IWMPSettings::getMode method</span></span>

<span data-ttu-id="67acf-107">O método **GetMode** retorna um valor que indica se o modo de loop ou o modo de ordem aleatória está ativo.</span><span class="sxs-lookup"><span data-stu-id="67acf-107">The **getMode** method returns a value indicating whether loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="67acf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67acf-108">Syntax</span></span>


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a><span data-ttu-id="67acf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67acf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67acf-110">*bstrmode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="67acf-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67acf-111">Um **System. String** que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="67acf-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="67acf-112">Valor</span><span class="sxs-lookup"><span data-stu-id="67acf-112">Value</span></span>      | <span data-ttu-id="67acf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="67acf-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67acf-114">rebobinar</span><span class="sxs-lookup"><span data-stu-id="67acf-114">autoRewind</span></span> | <span data-ttu-id="67acf-115">As faixas são reiniciadas desde o início após a execução até o final.</span><span class="sxs-lookup"><span data-stu-id="67acf-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="67acf-116">loop</span><span class="sxs-lookup"><span data-stu-id="67acf-116">loop</span></span>       | <span data-ttu-id="67acf-117">A sequência de faixas se repete.</span><span class="sxs-lookup"><span data-stu-id="67acf-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="67acf-118">conmoldura</span><span class="sxs-lookup"><span data-stu-id="67acf-118">showFrame</span></span>  | <span data-ttu-id="67acf-119">O quadro de chave mais próximo é exibido quando não está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="67acf-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="67acf-120">Esse modo não é relevante para faixas de áudio.</span><span class="sxs-lookup"><span data-stu-id="67acf-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="67acf-121">ordem aleatória</span><span class="sxs-lookup"><span data-stu-id="67acf-121">shuffle</span></span>    | <span data-ttu-id="67acf-122">As faixas são reproduzidas em ordem aleatória.</span><span class="sxs-lookup"><span data-stu-id="67acf-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67acf-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67acf-123">Return value</span></span>

<span data-ttu-id="67acf-124">Um valor **System. booliano** que indica se o modo especificado está ativo.</span><span class="sxs-lookup"><span data-stu-id="67acf-124">A **System.Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="67acf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67acf-125">Requirements</span></span>



| <span data-ttu-id="67acf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="67acf-126">Requirement</span></span> | <span data-ttu-id="67acf-127">Valor</span><span class="sxs-lookup"><span data-stu-id="67acf-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67acf-128">Versão</span><span class="sxs-lookup"><span data-stu-id="67acf-128">Version</span></span><br/>   | <span data-ttu-id="67acf-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="67acf-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="67acf-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="67acf-130">Namespace</span></span><br/> | <span data-ttu-id="67acf-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="67acf-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="67acf-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="67acf-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="67acf-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="67acf-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67acf-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="67acf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67acf-135">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="67acf-135">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="67acf-136">**IWMPSettings. setMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="67acf-136">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





