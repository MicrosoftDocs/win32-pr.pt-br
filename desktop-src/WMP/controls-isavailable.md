---
title: Controls. IsAvailable
description: A propriedade IsAvailable indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada. | Controls. IsAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Controles. isdisponível Windows Media Player
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763362"
---
# <a name="controlsisavailable"></a><span data-ttu-id="a1b82-105">Controls. IsAvailable</span><span class="sxs-lookup"><span data-stu-id="a1b82-105">Controls.isAvailable</span></span>

<span data-ttu-id="a1b82-106">A propriedade **IsAvailable** indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="a1b82-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="a1b82-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1b82-107">Parameters</span></span>

<span data-ttu-id="a1b82-108">*name*</span><span class="sxs-lookup"><span data-stu-id="a1b82-108">*name*</span></span>

<span data-ttu-id="a1b82-109">**Cadeia de caracteres** que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1b82-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="a1b82-110">String</span><span class="sxs-lookup"><span data-stu-id="a1b82-110">String</span></span>          | <span data-ttu-id="a1b82-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1b82-111">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b82-112">currentItem</span><span class="sxs-lookup"><span data-stu-id="a1b82-112">currentItem</span></span>     | <span data-ttu-id="a1b82-113">Determina se o usuário pode definir a propriedade **currentItem** .</span><span class="sxs-lookup"><span data-stu-id="a1b82-113">Determines whether the user can set the **currentItem** property.</span></span>                                                                                                 |
| <span data-ttu-id="a1b82-114">currentMarker</span><span class="sxs-lookup"><span data-stu-id="a1b82-114">currentMarker</span></span>   | <span data-ttu-id="a1b82-115">Determina se o usuário pode buscar um marcador específico.</span><span class="sxs-lookup"><span data-stu-id="a1b82-115">Determines whether the user can seek to a specific marker.</span></span>                                                                                                        |
| <span data-ttu-id="a1b82-116">currentPosition</span><span class="sxs-lookup"><span data-stu-id="a1b82-116">currentPosition</span></span> | <span data-ttu-id="a1b82-117">Determina se o usuário pode buscar uma posição específica no arquivo.</span><span class="sxs-lookup"><span data-stu-id="a1b82-117">Determines whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="a1b82-118">Alguns arquivos não dão suporte à busca.</span><span class="sxs-lookup"><span data-stu-id="a1b82-118">Some files do not support seeking.</span></span>                                                       |
| <span data-ttu-id="a1b82-119">fastForward</span><span class="sxs-lookup"><span data-stu-id="a1b82-119">fastForward</span></span>     | <span data-ttu-id="a1b82-120">Determina se o arquivo dá suporte ao encaminhamento rápido e se essa funcionalidade pode ser invocada.</span><span class="sxs-lookup"><span data-stu-id="a1b82-120">Determines whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="a1b82-121">Muitos tipos de arquivo (ou transmissões ao vivo) não dão suporte a fastForward.</span><span class="sxs-lookup"><span data-stu-id="a1b82-121">Many file types (or live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="a1b82-122">fastReverse</span><span class="sxs-lookup"><span data-stu-id="a1b82-122">fastReverse</span></span>     | <span data-ttu-id="a1b82-123">Determina se o arquivo dá suporte a fastReverse e se essa funcionalidade pode ser invocada.</span><span class="sxs-lookup"><span data-stu-id="a1b82-123">Determines whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="a1b82-124">Muitos tipos de arquivo (ou transmissões ao vivo) não dão suporte a fastReverse.</span><span class="sxs-lookup"><span data-stu-id="a1b82-124">Many file types (or live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="a1b82-125">Próximo</span><span class="sxs-lookup"><span data-stu-id="a1b82-125">next</span></span>            | <span data-ttu-id="a1b82-126">Determina se o usuário pode buscar a próxima entrada em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a1b82-126">Determines whether the user can seek to the next entry in a playlist.</span></span>                                                                                             |
| <span data-ttu-id="a1b82-127">pause</span><span class="sxs-lookup"><span data-stu-id="a1b82-127">pause</span></span>           | <span data-ttu-id="a1b82-128">Determina se o método **Pause** está disponível.</span><span class="sxs-lookup"><span data-stu-id="a1b82-128">Determines whether the **pause** method is available.</span></span>                                                                                                             |
| <span data-ttu-id="a1b82-129">jogar</span><span class="sxs-lookup"><span data-stu-id="a1b82-129">play</span></span>            | <span data-ttu-id="a1b82-130">Determina se o método **Play** está disponível.</span><span class="sxs-lookup"><span data-stu-id="a1b82-130">Determines whether the **play** method is available.</span></span>                                                                                                              |
| <span data-ttu-id="a1b82-131">previous</span><span class="sxs-lookup"><span data-stu-id="a1b82-131">previous</span></span>        | <span data-ttu-id="a1b82-132">Determina se o usuário pode buscar a entrada anterior em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a1b82-132">Determines whether the user can seek to the previous entry in a playlist.</span></span>                                                                                         |
| <span data-ttu-id="a1b82-133">Etapa</span><span class="sxs-lookup"><span data-stu-id="a1b82-133">step</span></span>            | <span data-ttu-id="a1b82-134">Determina se o método **Step** está disponível durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="a1b82-134">Determines whether the **step** method is available during playback.</span></span>                                                                                              |
| <span data-ttu-id="a1b82-135">parar</span><span class="sxs-lookup"><span data-stu-id="a1b82-135">stop</span></span>            | <span data-ttu-id="a1b82-136">Determina se o método **Stop** está disponível.</span><span class="sxs-lookup"><span data-stu-id="a1b82-136">Determines whether the **stop** method is available.</span></span>                                                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="a1b82-137">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a1b82-137">Return Values</span></span>

<span data-ttu-id="a1b82-138">Esse método retorna um valor **booliano** .</span><span class="sxs-lookup"><span data-stu-id="a1b82-138">This method returns a **Boolean** value.</span></span>

## <a name="examples"></a><span data-ttu-id="a1b82-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1b82-139">Examples</span></span>

<span data-ttu-id="a1b82-140">O exemplo a seguir cria um elemento de botão HTML que busca a posição inicial do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="a1b82-140">The following example creates an HTML BUTTON element that seeks to the starting position of the current media item.</span></span> <span data-ttu-id="a1b82-141">O código JScript usa **IsAvailable** para verificar se o arquivo dá suporte à operação de busca.</span><span class="sxs-lookup"><span data-stu-id="a1b82-141">The JScript code uses **isAvailable** to verify that the file supports the seek operation.</span></span> <span data-ttu-id="a1b82-142">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a1b82-142">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a><span data-ttu-id="a1b82-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1b82-143">Requirements</span></span>



| <span data-ttu-id="a1b82-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1b82-144">Requirement</span></span> | <span data-ttu-id="a1b82-145">Valor</span><span class="sxs-lookup"><span data-stu-id="a1b82-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b82-146">Versão</span><span class="sxs-lookup"><span data-stu-id="a1b82-146">Version</span></span><br/> | <span data-ttu-id="a1b82-147">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a1b82-147">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="a1b82-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a1b82-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1b82-149"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1b82-149"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b82-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1b82-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b82-151">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="a1b82-151">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





