---
description: O Direct3D mantém uma lista de até oito texturas atuais. Ele mistura essas texturas em todos os primitivos que renderiza. Somente as texturas criadas como ponteiros de interface de textura podem ser usadas no conjunto de texturas atuais.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Atribuindo as texturas atuais (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457190"
---
# <a name="assigning-the-current-textures-direct3d-9"></a><span data-ttu-id="b538a-105">Atribuindo as texturas atuais (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b538a-105">Assigning the Current Textures (Direct3D 9)</span></span>

<span data-ttu-id="b538a-106">O Direct3D mantém uma lista de até oito texturas atuais.</span><span class="sxs-lookup"><span data-stu-id="b538a-106">Direct3D maintains a list of up to eight current textures.</span></span> <span data-ttu-id="b538a-107">Ele mistura essas texturas em todos os primitivos que renderiza.</span><span class="sxs-lookup"><span data-stu-id="b538a-107">It blends these textures onto all the primitive it renders.</span></span> <span data-ttu-id="b538a-108">Somente as texturas criadas como ponteiros de interface de textura podem ser usadas no conjunto de texturas atuais.</span><span class="sxs-lookup"><span data-stu-id="b538a-108">Only textures created as texture interface pointers can be used in the set of current textures.</span></span>

<span data-ttu-id="b538a-109">Os aplicativos chamam o método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para atribuir texturas ao conjunto de texturas atuais.</span><span class="sxs-lookup"><span data-stu-id="b538a-109">Applications call the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method to assign textures into the set of current textures.</span></span> <span data-ttu-id="b538a-110">O primeiro parâmetro deve ser um número no intervalo de 0-7, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b538a-110">The first parameter must be a number in the range of 0-7, inclusive.</span></span> <span data-ttu-id="b538a-111">Passe o ponteiro da interface de textura como o segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b538a-111">Pass the texture interface pointer as the second parameter.</span></span>

<span data-ttu-id="b538a-112">O exemplo de código C++ a seguir demonstra como uma textura pode ser atribuída ao conjunto de texturas atuais.</span><span class="sxs-lookup"><span data-stu-id="b538a-112">The following C++ code example demonstrates how a texture can be assigned to the set of current textures.</span></span>


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> <span data-ttu-id="b538a-113">Os dispositivos de software não dão suporte à atribuição de uma textura a mais de um estágio de textura por vez.</span><span class="sxs-lookup"><span data-stu-id="b538a-113">Software devices do not support assigning a texture to more than one texture stage at a time.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b538a-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b538a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b538a-115">Mesclagem de textura</span><span class="sxs-lookup"><span data-stu-id="b538a-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
