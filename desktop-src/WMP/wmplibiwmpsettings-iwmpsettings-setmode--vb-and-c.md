---
title: Método setmode IWMPSettings
description: O método setmode define o modo de loop ou de ordem aleatória como ativo ou inativo.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- método setmode do Windows Media Player
- método setmode Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, método setmode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764169"
---
# <a name="iwmpsettingssetmode-method"></a><span data-ttu-id="50084-106">Método IWMPSettings:: setmode</span><span class="sxs-lookup"><span data-stu-id="50084-106">IWMPSettings::setMode method</span></span>

<span data-ttu-id="50084-107">O método **setmode** define o modo de loop ou de ordem aleatória como ativo ou inativo.</span><span class="sxs-lookup"><span data-stu-id="50084-107">The **setMode** method sets the loop mode or shuffle mode to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="50084-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50084-108">Syntax</span></span>


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a><span data-ttu-id="50084-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50084-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50084-110">*bstrmode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50084-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50084-111">Um **System. String** que é o nome do modo que está sendo alterado, contendo um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="50084-111">A **System.String** that is the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="50084-112">Valor</span><span class="sxs-lookup"><span data-stu-id="50084-112">Value</span></span>      | <span data-ttu-id="50084-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="50084-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50084-114">rebobinar</span><span class="sxs-lookup"><span data-stu-id="50084-114">autoRewind</span></span> | <span data-ttu-id="50084-115">As faixas são reiniciadas desde o início após a execução até o final.</span><span class="sxs-lookup"><span data-stu-id="50084-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="50084-116">loop</span><span class="sxs-lookup"><span data-stu-id="50084-116">loop</span></span>       | <span data-ttu-id="50084-117">A sequência de faixas se repete.</span><span class="sxs-lookup"><span data-stu-id="50084-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="50084-118">conmoldura</span><span class="sxs-lookup"><span data-stu-id="50084-118">showFrame</span></span>  | <span data-ttu-id="50084-119">O quadro de chave mais próximo é exibido quando não está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="50084-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="50084-120">Esse modo não é relevante para faixas de áudio.</span><span class="sxs-lookup"><span data-stu-id="50084-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="50084-121">ordem aleatória</span><span class="sxs-lookup"><span data-stu-id="50084-121">shuffle</span></span>    | <span data-ttu-id="50084-122">As faixas são reproduzidas em ordem aleatória.</span><span class="sxs-lookup"><span data-stu-id="50084-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> <dt>

<span data-ttu-id="50084-123">*varfMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50084-123">*varfMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50084-124">Um valor **System. Boolean** que especifica se o novo modo especificado está ativo.</span><span class="sxs-lookup"><span data-stu-id="50084-124">A **System.Boolean** value specifying whether the new specified mode is active.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50084-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50084-125">Return value</span></span>

<span data-ttu-id="50084-126">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="50084-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50084-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="50084-127">Remarks</span></span>

<span data-ttu-id="50084-128">Quando o modo de conmoldura está ativo, o Windows Media Player deve acessar o conteúdo de acompanhamento para recuperar o quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="50084-128">When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="50084-129">Use esse modo com cuidado ao reproduzir conteúdo que não seja local.</span><span class="sxs-lookup"><span data-stu-id="50084-129">Use this mode cautiously when playing content that is not local.</span></span>

## <a name="requirements"></a><span data-ttu-id="50084-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50084-130">Requirements</span></span>



| <span data-ttu-id="50084-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="50084-131">Requirement</span></span> | <span data-ttu-id="50084-132">Valor</span><span class="sxs-lookup"><span data-stu-id="50084-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50084-133">Versão</span><span class="sxs-lookup"><span data-stu-id="50084-133">Version</span></span><br/>   | <span data-ttu-id="50084-134">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="50084-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="50084-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="50084-135">Namespace</span></span><br/> | <span data-ttu-id="50084-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="50084-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="50084-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="50084-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="50084-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="50084-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50084-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="50084-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50084-140">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="50084-140">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="50084-141">**IWMPSettings. GetMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="50084-141">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





