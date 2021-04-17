---
title: THEME. loadpreference
description: O método loadpreference carrega uma preferência do registro.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- THEME. loadpreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782220"
---
# <a name="themeloadpreference"></a><span data-ttu-id="0aa68-104">THEME. loadpreference</span><span class="sxs-lookup"><span data-stu-id="0aa68-104">THEME.loadPreference</span></span>

<span data-ttu-id="0aa68-105">O método **loadpreference** carrega uma preferência do registro.</span><span class="sxs-lookup"><span data-stu-id="0aa68-105">The **loadPreference** method loads a preference from the registry.</span></span>

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a><span data-ttu-id="0aa68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0aa68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa68-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="0aa68-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="0aa68-108">Uma **cadeia de caracteres** que especifica a chave do valor de preferência a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="0aa68-108">A **String** specifying the key of the preference value to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa68-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0aa68-109">Return Value</span></span>

<span data-ttu-id="0aa68-110">Esse método retorna uma **cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="0aa68-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aa68-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0aa68-111">Remarks</span></span>

<span data-ttu-id="0aa68-112">Uma preferência é um par chave/valor que pode ser armazenado no registro para reter informações sobre o estado do Windows Media Player entre execuções.</span><span class="sxs-lookup"><span data-stu-id="0aa68-112">A preference is a key/value pair that can be stored in the registry to retain information about the state of the Windows Media Player between runs.</span></span> <span data-ttu-id="0aa68-113">Esse recurso pode ser usado, por exemplo, para salvar configurações de personalização para que elas não precisem ser reinseridas sempre que o Windows Media Player for iniciado.</span><span class="sxs-lookup"><span data-stu-id="0aa68-113">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="0aa68-114">As preferências não são criptografadas e, portanto, não são um método seguro para persistir dados.</span><span class="sxs-lookup"><span data-stu-id="0aa68-114">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="0aa68-115">Não use as preferências para armazenar dados privados.</span><span class="sxs-lookup"><span data-stu-id="0aa68-115">Do not use preferences to store private data.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa68-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa68-116">Requirements</span></span>



| <span data-ttu-id="0aa68-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa68-117">Requirement</span></span> | <span data-ttu-id="0aa68-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0aa68-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0aa68-119">Versão</span><span class="sxs-lookup"><span data-stu-id="0aa68-119">Version</span></span><br/> | <span data-ttu-id="0aa68-120">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0aa68-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0aa68-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0aa68-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa68-122">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="0aa68-122">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="0aa68-123">**THEME. savePreference**</span><span class="sxs-lookup"><span data-stu-id="0aa68-123">**THEME.savePreference**</span></span>](theme-savepreference.md)
</dt> </dl>

 

 





