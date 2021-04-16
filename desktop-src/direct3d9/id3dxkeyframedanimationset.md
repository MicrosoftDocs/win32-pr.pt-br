---
description: Um aplicativo usa os métodos dessa interface para implementar um conjunto de animações de quadro chave.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Interface ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789616"
---
# <a name="id3dxkeyframedanimationset-interface"></a><span data-ttu-id="c3a85-103">Interface ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="c3a85-103">ID3DXKeyframedAnimationSet interface</span></span>

<span data-ttu-id="c3a85-104">Um aplicativo usa os métodos dessa interface para implementar um conjunto de animações de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="c3a85-104">An application uses the methods of this interface to implement a key frame animation set.</span></span>

## <a name="members"></a><span data-ttu-id="c3a85-105">Membros</span><span class="sxs-lookup"><span data-stu-id="c3a85-105">Members</span></span>

<span data-ttu-id="c3a85-106">A interface **ID3DXKeyframedAnimationSet** herda de [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="c3a85-106">The **ID3DXKeyframedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="c3a85-107">**ID3DXKeyframedAnimationSet** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c3a85-107">**ID3DXKeyframedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="c3a85-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3a85-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c3a85-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3a85-109">Methods</span></span>

<span data-ttu-id="c3a85-110">A interface **ID3DXKeyframedAnimationSet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c3a85-110">The **ID3DXKeyframedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="c3a85-111">Método</span><span class="sxs-lookup"><span data-stu-id="c3a85-111">Method</span></span>                                                                                   | <span data-ttu-id="c3a85-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3a85-112">Description</span></span>                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3a85-113">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="c3a85-113">**Compress**</span></span>](id3dxkeyframedanimationset--compress.md)                                 | <span data-ttu-id="c3a85-114">Transforma animações em uma animação definida em um formato compactado e retorna um ponteiro para o buffer que armazena os dados compactados.</span><span class="sxs-lookup"><span data-stu-id="c3a85-114">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span><br/> |
| [<span data-ttu-id="c3a85-115">**GetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-115">**GetCallbackKey**</span></span>](id3dxkeyframedanimationset--getcallbackkey.md)                     | <span data-ttu-id="c3a85-116">Obtém informações sobre um retorno de chamada específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-116">Gets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="c3a85-117">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-117">**GetCallbackKeys**</span></span>](id3dxkeyframedanimationset--getcallbackkeys.md)                   | <span data-ttu-id="c3a85-118">Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="c3a85-118">Fills an array with callback key data used for key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="c3a85-119">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-119">**GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | <span data-ttu-id="c3a85-120">Obtém o número de chaves de retorno de chamada no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-120">Gets the number of callback keys in the animation set.</span></span><br/>                                                                                  |
| [<span data-ttu-id="c3a85-121">**GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-121">**GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)             | <span data-ttu-id="c3a85-122">Obtém o número de chaves de rotação na animação do quadro chave especificado.</span><span class="sxs-lookup"><span data-stu-id="c3a85-122">Gets the number of rotation keys in the specified key frame animation.</span></span><br/>                                                                  |
| [<span data-ttu-id="c3a85-123">**GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-123">**GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)                   | <span data-ttu-id="c3a85-124">Obtém o número de chaves de escala na animação do quadro chave especificado.</span><span class="sxs-lookup"><span data-stu-id="c3a85-124">Gets the number of scale keys in the specified key frame animation.</span></span><br/>                                                                     |
| [<span data-ttu-id="c3a85-125">**GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-125">**GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | <span data-ttu-id="c3a85-126">Obtém o número de chaves de tradução na animação do quadro chave especificado.</span><span class="sxs-lookup"><span data-stu-id="c3a85-126">Gets the number of translation keys in the specified key frame animation.</span></span><br/>                                                               |
| [<span data-ttu-id="c3a85-127">**Getreproduzirtype**</span><span class="sxs-lookup"><span data-stu-id="c3a85-127">**GetPlaybackType**</span></span>](id3dxkeyframedanimationset--getplaybacktype.md)                   | <span data-ttu-id="c3a85-128">Obtém o tipo do loop de reprodução do conjunto de animação.</span><span class="sxs-lookup"><span data-stu-id="c3a85-128">Gets the type of the animation set playback loop.</span></span><br/>                                                                                       |
| [<span data-ttu-id="c3a85-129">**GetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-129">**GetRotationKey**</span></span>](id3dxkeyframedanimationset--getrotationkey.md)                     | <span data-ttu-id="c3a85-130">Obter informações de rotação para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-130">Get rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="c3a85-131">**GetRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-131">**GetRotationKeys**</span></span>](id3dxkeyframedanimationset--getrotationkeys.md)                   | <span data-ttu-id="c3a85-132">Preenche uma matriz com dados de chave de rotação usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="c3a85-132">Fills an array with rotational key data used for key frame animation.</span></span><br/>                                                                   |
| [<span data-ttu-id="c3a85-133">**GetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-133">**GetScaleKey**</span></span>](id3dxkeyframedanimationset--getscalekey.md)                           | <span data-ttu-id="c3a85-134">Obter informações de escala para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-134">Get scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="c3a85-135">**GetScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-135">**GetScaleKeys**</span></span>](id3dxkeyframedanimationset--getscalekeys.md)                         | <span data-ttu-id="c3a85-136">Preenche uma matriz com dados de chave de escala usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="c3a85-136">Fills an array with scale key data used for key frame animation.</span></span><br/>                                                                        |
| [<span data-ttu-id="c3a85-137">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="c3a85-137">**GetSourceTicksPerSecond**</span></span>](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | <span data-ttu-id="c3a85-138">Obtém o número de tiques de quadros-chave de animação que ocorrem por segundo.</span><span class="sxs-lookup"><span data-stu-id="c3a85-138">Gets the number of animation key frame ticks that occur per second.</span></span><br/>                                                                     |
| [<span data-ttu-id="c3a85-139">**GetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-139">**GetTranslationKey**</span></span>](id3dxkeyframedanimationset--gettranslationkey.md)               | <span data-ttu-id="c3a85-140">Obter informações de tradução para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-140">Get translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="c3a85-141">**GetTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-141">**GetTranslationKeys**</span></span>](id3dxkeyframedanimationset--gettranslationkeys.md)             | <span data-ttu-id="c3a85-142">Preenche uma matriz com dados de chave de tradução usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="c3a85-142">Fills an array with translational key data used for key frame animation.</span></span><br/>                                                                |
| [<span data-ttu-id="c3a85-143">**RegisterAnimationSRTKeys**</span><span class="sxs-lookup"><span data-stu-id="c3a85-143">**RegisterAnimationSRTKeys**</span></span>](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | <span data-ttu-id="c3a85-144">Registre os dados de quadro-chave de dimensionamento, rotação e conversão (SRT) para uma animação.</span><span class="sxs-lookup"><span data-stu-id="c3a85-144">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span><br/>                                                        |
| [<span data-ttu-id="c3a85-145">**SetCallbackKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-145">**SetCallbackKey**</span></span>](id3dxkeyframedanimationset--setcallbackkey.md)                     | <span data-ttu-id="c3a85-146">Define informações sobre um retorno de chamada específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-146">Sets information about a specific callback in the animation set.</span></span><br/>                                                                        |
| [<span data-ttu-id="c3a85-147">**SetRotationKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-147">**SetRotationKey**</span></span>](id3dxkeyframedanimationset--setrotationkey.md)                     | <span data-ttu-id="c3a85-148">Defina informações de rotação para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-148">Set rotation information for a specific key frame in the animation set.</span></span><br/>                                                                 |
| [<span data-ttu-id="c3a85-149">**SetScaleKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-149">**SetScaleKey**</span></span>](id3dxkeyframedanimationset--setscalekey.md)                           | <span data-ttu-id="c3a85-150">Defina informações de escala para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-150">Set scale information for a specific key frame in the animation set.</span></span><br/>                                                                    |
| [<span data-ttu-id="c3a85-151">**SetTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-151">**SetTranslationKey**</span></span>](id3dxkeyframedanimationset--settranslationkey.md)               | <span data-ttu-id="c3a85-152">Definir informações de tradução para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-152">Set translation information for a specific key frame in the animation set.</span></span><br/>                                                              |
| [<span data-ttu-id="c3a85-153">**UnregisterAnimation**</span><span class="sxs-lookup"><span data-stu-id="c3a85-153">**UnregisterAnimation**</span></span>](id3dxkeyframedanimationset--unregisteranimation.md)           | <span data-ttu-id="c3a85-154">Remova os dados de animação do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="c3a85-154">Remove the animation data from the animation set.</span></span><br/>                                                                                       |
| [<span data-ttu-id="c3a85-155">**UnregisterRotationKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-155">**UnregisterRotationKey**</span></span>](id3dxkeyframedanimationset--unregisterrotationkey.md)       | <span data-ttu-id="c3a85-156">Remove os dados de rotação no quadro de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="c3a85-156">Removes the rotation data at the specified key frame.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c3a85-157">**UnregisterScaleKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-157">**UnregisterScaleKey**</span></span>](id3dxkeyframedanimationset--unregisterscalekey.md)             | <span data-ttu-id="c3a85-158">Remove os dados de escala no quadro de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="c3a85-158">Removes the scale data at the specified key frame.</span></span><br/>                                                                                      |
| [<span data-ttu-id="c3a85-159">**UnregisterTranslationKey**</span><span class="sxs-lookup"><span data-stu-id="c3a85-159">**UnregisterTranslationKey**</span></span>](id3dxkeyframedanimationset--unregistertranslationkey.md) | <span data-ttu-id="c3a85-160">Remove os dados de tradução no quadro de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="c3a85-160">Removes the translation data at the specified key frame.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="c3a85-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a85-161">Remarks</span></span>

<span data-ttu-id="c3a85-162">Crie uma animação de quadro chave definida com [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="c3a85-162">Create a keyframed animation set with [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).</span></span>

<span data-ttu-id="c3a85-163">O tipo LPD3DXKEYFRAMEDANIMATIONSET é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="c3a85-163">The LPD3DXKEYFRAMEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="c3a85-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3a85-164">Requirements</span></span>



| <span data-ttu-id="c3a85-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a85-165">Requirement</span></span> | <span data-ttu-id="c3a85-166">Valor</span><span class="sxs-lookup"><span data-stu-id="c3a85-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a85-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3a85-167">Header</span></span><br/>  | <dl> <span data-ttu-id="c3a85-168"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3a85-168"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c3a85-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3a85-169">Library</span></span><br/> | <dl> <span data-ttu-id="c3a85-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3a85-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3a85-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3a85-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a85-172">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="c3a85-172">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="c3a85-173">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="c3a85-173">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




