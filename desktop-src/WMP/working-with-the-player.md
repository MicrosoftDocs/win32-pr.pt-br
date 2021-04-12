---
title: Trabalhando com o Player
description: Trabalhando com o Player
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Capas do Windows Media Player, atributo Player no JScript
- capas, atributo Player em JScript
- atributos, Player
- atributo do Player
- Arquivos JScript para capas, atributo Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364448"
---
# <a name="working-with-the-player"></a><span data-ttu-id="63a56-108">Trabalhando com o Player</span><span class="sxs-lookup"><span data-stu-id="63a56-108">Working with the Player</span></span>

<span data-ttu-id="63a56-109">Ao usar o Microsoft JScript para acessar métodos e propriedades do Windows Media Player, você deve usar o nome "Player" para o nome do controle.</span><span class="sxs-lookup"><span data-stu-id="63a56-109">When using Microsoft JScript to access methods and properties of Windows Media Player, you must use the name "player" for the name of the control.</span></span> <span data-ttu-id="63a56-110">Por exemplo, para fazer referência ao método stop, você deve digitar:</span><span class="sxs-lookup"><span data-stu-id="63a56-110">For example, to reference the Stop method, you must type:</span></span>


```C++
player.Controls.Stop()

```



<span data-ttu-id="63a56-111">O atributo global do **Player** é a chave para acessar o controle do Windows Media Player por meio de script de capa.</span><span class="sxs-lookup"><span data-stu-id="63a56-111">The **player** global attribute is the key to accessing the Windows Media Player control through skin scripting.</span></span> <span data-ttu-id="63a56-112">Por meio desse atributo, todos os objetos do controle do Windows Media Player tornam-se acessíveis para a modificação de tempo de execução por meio de suas propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="63a56-112">Through this attribute, all the objects of the Windows Media Player control become accessible for run-time modification through their properties and methods.</span></span> <span data-ttu-id="63a56-113">Além disso, o elemento **Player** está disponível para que você possa especificar manipuladores de eventos e o atributo **URL** em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="63a56-113">Additionally, the **PLAYER** element is available so that you can specify event handlers and the **url** attribute at design time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63a56-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63a56-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63a56-115">**Usando o JScript**</span><span class="sxs-lookup"><span data-stu-id="63a56-115">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




