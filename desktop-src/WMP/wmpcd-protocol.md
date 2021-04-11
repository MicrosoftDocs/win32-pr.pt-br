---
title: Protocolo WMPCD
description: Protocolo WMPCD
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player, protocolos
- Modelo de objeto do Windows Media Player, protocolos
- modelo de objeto, protocolos
- Controle ActiveX do Windows Media Player, protocolos para o modelo de objeto
- Controle ActiveX, protocolos para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, protocolos para modelo de objeto
- Windows Media Player Mobile, protocolos para modelo de objeto
- protocolos, modelo de objeto do Windows Media Player
- protocolos, WMPCD
- Protocolo WMPCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159762"
---
# <a name="wmpcd-protocol"></a><span data-ttu-id="44555-113">Protocolo WMPCD</span><span class="sxs-lookup"><span data-stu-id="44555-113">WMPCD Protocol</span></span>

<span data-ttu-id="44555-114">O protocolo WMPCD permite que você especifique faixas em um CD usando a sintaxe de URL.</span><span class="sxs-lookup"><span data-stu-id="44555-114">The WMPCD protocol enables you to specify tracks on a compact disc using URL syntax.</span></span> <span data-ttu-id="44555-115">Esta é a sintaxe geral do protocolo:</span><span class="sxs-lookup"><span data-stu-id="44555-115">This is the general syntax of the protocol:</span></span>


```C++
wmpcd://drive/track
```



<span data-ttu-id="44555-116">O segmento da *unidade* é o índice da unidade de CD.</span><span class="sxs-lookup"><span data-stu-id="44555-116">The *drive* segment is the index of the CD drive.</span></span> <span data-ttu-id="44555-117">O segmento de *faixa* é o número da faixa. O exemplo a seguir demonstra o uso do protocolo WMPCD.</span><span class="sxs-lookup"><span data-stu-id="44555-117">The *track* segment is the number of the track. The following example demonstrates using the WMPCD protocol.</span></span>


```C++
player.url = "wmpcd://0/4";
```



<span data-ttu-id="44555-118">O exemplo reproduz a quarta faixa no disco na primeira unidade de CD (a unidade cujo índice é 0).</span><span class="sxs-lookup"><span data-stu-id="44555-118">The example plays the fourth track on the disc in the first CD drive (the drive whose index is 0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="44555-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44555-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44555-120">**Tipos de arquivos e protocolos com suporte**</span><span class="sxs-lookup"><span data-stu-id="44555-120">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




