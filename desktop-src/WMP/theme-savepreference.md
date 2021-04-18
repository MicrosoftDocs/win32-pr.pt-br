---
title: THEME. savePreference
description: O método savePreference salva uma preferência no registro.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEME. savePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780249"
---
# <a name="themesavepreference"></a><span data-ttu-id="d701e-104">THEME. savePreference</span><span class="sxs-lookup"><span data-stu-id="d701e-104">THEME.savePreference</span></span>

<span data-ttu-id="d701e-105">O método **savePreference** salva uma preferência no registro.</span><span class="sxs-lookup"><span data-stu-id="d701e-105">The **savePreference** method saves a preference in the registry.</span></span>

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a><span data-ttu-id="d701e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d701e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d701e-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="d701e-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="d701e-108">Uma **cadeia de caracteres** que especifica a chave do valor de preferência a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="d701e-108">A **String** specifying the key of the preference value to save.</span></span>

</dd> <dt>

<span data-ttu-id="d701e-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*o valor*</span><span class="sxs-lookup"><span data-stu-id="d701e-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*</span></span>
</dt> <dd>

<span data-ttu-id="d701e-110">Uma **cadeia de caracteres** que especifica o valor a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="d701e-110">A **String** specifying the value to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d701e-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d701e-111">Return Value</span></span>

<span data-ttu-id="d701e-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d701e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d701e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d701e-113">Remarks</span></span>

<span data-ttu-id="d701e-114">Uma preferência é um par chave/valor que pode ser armazenado no registro para reter informações sobre o estado do Windows Media Player entre execuções.</span><span class="sxs-lookup"><span data-stu-id="d701e-114">A preference is a key/value pair that can be stored in the registry to retain information about the state of Windows Media Player between runs.</span></span> <span data-ttu-id="d701e-115">Esse recurso pode ser usado, por exemplo, para salvar configurações de personalização para que elas não precisem ser reinseridas sempre que o Windows Media Player for iniciado.</span><span class="sxs-lookup"><span data-stu-id="d701e-115">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="d701e-116">As preferências não são criptografadas e, portanto, não são um método seguro para persistir dados.</span><span class="sxs-lookup"><span data-stu-id="d701e-116">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="d701e-117">Não use as preferências para armazenar dados privados.</span><span class="sxs-lookup"><span data-stu-id="d701e-117">Do not use preferences to store private data.</span></span>

## <a name="examples"></a><span data-ttu-id="d701e-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d701e-118">Examples</span></span>


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="d701e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d701e-119">Requirements</span></span>



| <span data-ttu-id="d701e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d701e-120">Requirement</span></span> | <span data-ttu-id="d701e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d701e-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d701e-122">Versão</span><span class="sxs-lookup"><span data-stu-id="d701e-122">Version</span></span><br/> | <span data-ttu-id="d701e-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d701e-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d701e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d701e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d701e-125">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="d701e-125">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="d701e-126">**THEME. loadpreference**</span><span class="sxs-lookup"><span data-stu-id="d701e-126">**THEME.loadPreference**</span></span>](theme-loadpreference.md)
</dt> </dl>

 

 





