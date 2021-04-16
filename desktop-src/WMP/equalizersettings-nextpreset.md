---
title: EQUALIZERSETTINGS.nextPreset
description: O método nextPreset aplica a próxima predefinição de equalizador.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- EQUALIZERSETTINGS. nextPreset Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761097"
---
# <a name="equalizersettingsnextpreset"></a><span data-ttu-id="3cfd3-104">EQUALIZERSETTINGS.nextPreset</span><span class="sxs-lookup"><span data-stu-id="3cfd3-104">EQUALIZERSETTINGS.nextPreset</span></span>

<span data-ttu-id="3cfd3-105">O método **nextPreset** aplica a próxima predefinição de equalizador.</span><span class="sxs-lookup"><span data-stu-id="3cfd3-105">The **nextPreset** method applies the next equalizer preset.</span></span>

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a><span data-ttu-id="3cfd3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cfd3-106">Parameters</span></span>

<span data-ttu-id="3cfd3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3cfd3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cfd3-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3cfd3-108">Return Value</span></span>

<span data-ttu-id="3cfd3-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3cfd3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cfd3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cfd3-110">Remarks</span></span>

<span data-ttu-id="3cfd3-111">Se a predefinição atual for a última disponível, a primeira predefinição será tornada atual.</span><span class="sxs-lookup"><span data-stu-id="3cfd3-111">If the current preset is the last one available, the first preset is made current.</span></span>

## <a name="examples"></a><span data-ttu-id="3cfd3-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3cfd3-112">Examples</span></span>


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a><span data-ttu-id="3cfd3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cfd3-113">Requirements</span></span>



| <span data-ttu-id="3cfd3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cfd3-114">Requirement</span></span> | <span data-ttu-id="3cfd3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3cfd3-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3cfd3-116">Versão</span><span class="sxs-lookup"><span data-stu-id="3cfd3-116">Version</span></span><br/> | <span data-ttu-id="3cfd3-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3cfd3-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cfd3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cfd3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cfd3-119">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="3cfd3-119">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="3cfd3-120">**EQUALIZERSETTINGS.previousPreset**</span><span class="sxs-lookup"><span data-stu-id="3cfd3-120">**EQUALIZERSETTINGS.previousPreset**</span></span>](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





