---
description: O Direct3D 9 dá suporte a texturas de paletas por meio de um conjunto de 256 paletas de entrada associadas ao objeto IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Paletas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105796228"
---
# <a name="texture-palettes-direct3d-9"></a><span data-ttu-id="962b6-103">Paletas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="962b6-103">Texture Palettes (Direct3D 9)</span></span>

<span data-ttu-id="962b6-104">O Direct3D 9 dá suporte a texturas de paletas por meio de um conjunto de 256 paletas de entrada associadas ao objeto [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="962b6-104">Direct3D 9 supports paletted textures through a set of 256 entry palettes associated with the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) object.</span></span> <span data-ttu-id="962b6-105">Uma paleta é tornada atual chamando o método [**IDirect3DDevice9:: SetCurrentTexturePalette**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="962b6-105">A palette is made current by calling the [**IDirect3DDevice9::SetCurrentTexturePalette**](/windows/desktop/api) method.</span></span> <span data-ttu-id="962b6-106">A paleta atual é usada para traduzir todas as texturas da paleta para todos os estágios de textura ativas.</span><span class="sxs-lookup"><span data-stu-id="962b6-106">The current palette is used for translating all paletted textures for all active texture stages.</span></span> <span data-ttu-id="962b6-107">[**IDirect3DDevice9:: SetPaletteEntries**](/windows/desktop/api) atualiza todas as entradas 256 de uma paleta.</span><span class="sxs-lookup"><span data-stu-id="962b6-107">[**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) updates all of a palette's 256 entries.</span></span> <span data-ttu-id="962b6-108">Cada entrada é uma estrutura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) do formato D3DFMT \_ A8R8G8B8.</span><span class="sxs-lookup"><span data-stu-id="962b6-108">Each entry is a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure of the format D3DFMT\_A8R8G8B8.</span></span> <span data-ttu-id="962b6-109">Todas as entradas assumem o padrão de 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="962b6-109">All entries default to 0xFFFFFFFF.</span></span>

<span data-ttu-id="962b6-110">As paletas [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contêm um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="962b6-110">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) palettes contain an alpha channel.</span></span> <span data-ttu-id="962b6-111">Esse canal alfa pode ser usado quando o \_ sinalizador de recurso de dispositivo D3DPTEXTURECAPS ALPHAPALETTE é definido, indicando que o dispositivo dá suporte a alfa da paleta.</span><span class="sxs-lookup"><span data-stu-id="962b6-111">This alpha channel can be used when the D3DPTEXTURECAPS\_ALPHAPALETTE device capability flag is set, indicating that the device supports alpha from the palette.</span></span> <span data-ttu-id="962b6-112">O canal alfa da paleta é usado quando o formato de textura não tem um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="962b6-112">The palette alpha channel is used when the texture format does not have an alpha channel.</span></span> <span data-ttu-id="962b6-113">Se o dispositivo não oferecer suporte a alfa da paleta e o formato de textura não tiver um canal alfa, um valor de 0xFF será usado para alfa.</span><span class="sxs-lookup"><span data-stu-id="962b6-113">If the device does not support alpha from the palette and the texture format does not have an alpha channel, then a value of 0xFF is used for alpha.</span></span>

<span data-ttu-id="962b6-114">Há um máximo de 65.536 de paletas (0x0000FFFF).</span><span class="sxs-lookup"><span data-stu-id="962b6-114">There is a maximum of 65,536 (0x0000FFFF) palettes.</span></span> <span data-ttu-id="962b6-115">Como os recursos de memória associados ao conjunto de paletas são proporcionais ao número máximo de paleta que um aplicativo faz referência, use números de paleta contíguos começando em zero.</span><span class="sxs-lookup"><span data-stu-id="962b6-115">Because memory resources associated with the set of palettes are proportional to the maximum palette number that an application references, use contiguous palette numbers starting at zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="962b6-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="962b6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="962b6-117">Conceitos básicos de texturing</span><span class="sxs-lookup"><span data-stu-id="962b6-117">Basic Texturing Concepts</span></span>](basic-texturing-concepts.md)
</dt> </dl>

 

 
