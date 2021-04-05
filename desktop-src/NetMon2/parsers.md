---
description: Um analisador é o componente Monitor de Rede que inspeciona dados em uma captura atrasada e passa informações de protocolo específicas para o aplicativo que chama o analisador. Um analisador é passivo porque funciona somente quando Monitor de Rede ou um especialista o chama.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74aa86a17e87ab139ad48583285da943f23d330c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826825"
---
# <a name="parser"></a><span data-ttu-id="6ad23-104">Analisador</span><span class="sxs-lookup"><span data-stu-id="6ad23-104">Parser</span></span>

<span data-ttu-id="6ad23-105">Um analisador é o componente Monitor de Rede que inspeciona dados em uma [*captura atrasada*](d.md)e passa informações de protocolo específicas para o aplicativo que chama o analisador.</span><span class="sxs-lookup"><span data-stu-id="6ad23-105">A parser is the Network Monitor component that inspects data in a [*delayed capture*](d.md), and passes specific protocol information to the application that calls the parser.</span></span> <span data-ttu-id="6ad23-106">Um analisador é passivo porque funciona somente quando Monitor de Rede ou um [*especialista*](e.md) o chama.</span><span class="sxs-lookup"><span data-stu-id="6ad23-106">A parser is passive because it works only when Network Monitor or an [*expert*](e.md) call it.</span></span>

<span data-ttu-id="6ad23-107">Cada analisador identifica um protocolo e, normalmente, um analisador é implementado em sua própria DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="6ad23-107">Each parser identifies one protocol, and typically, a parser is implemented within its own parser DLL.</span></span> <span data-ttu-id="6ad23-108">No entanto, uma DLL do analisador pode conter vários analisadores, o que significa que uma DLL pode ser usada para detectar mais de um protocolo.</span><span class="sxs-lookup"><span data-stu-id="6ad23-108">However, a parser DLL can contain multiple parsers which means that one DLL can be used to detect more than one protocol.</span></span>

<span data-ttu-id="6ad23-109">Os dados passados para um analisador são tirados de uma [*captura atrasada*](d.md)e passados para o analisador em uma base quadro a quadro.</span><span class="sxs-lookup"><span data-stu-id="6ad23-109">The data passed to a parser is taken from a [*delayed capture*](d.md), and passed to the parser on a frame-by-frame basis.</span></span> <span data-ttu-id="6ad23-110">Você não pode analisar uma captura em tempo real.</span><span class="sxs-lookup"><span data-stu-id="6ad23-110">You cannot parse a real-time capture.</span></span>

<span data-ttu-id="6ad23-111">Para analisar os dados em um quadro, o analisador deve reconhecer a instância de protocolo, identificar as propriedades que existem na instância de protocolo e anexar uma definição de propriedade a cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="6ad23-111">To parse the data in a frame, the parser must recognize the protocol instance, identify the properties that exist in the protocol instance, and attach a property definition to each property.</span></span> <span data-ttu-id="6ad23-112">Lembre-se de que o quadro contém apenas um fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="6ad23-112">Be aware that the frame contains only a stream of data.</span></span> <span data-ttu-id="6ad23-113">O quadro não contém dados que indicam quais protocolos ou propriedades de protocolo os dados representam.</span><span class="sxs-lookup"><span data-stu-id="6ad23-113">The frame does not contain data that indicates which protocols or protocol properties the data represents.</span></span>

<span data-ttu-id="6ad23-114">A ilustração a seguir mostra um quadro que contém uma instância de um protocolo.</span><span class="sxs-lookup"><span data-stu-id="6ad23-114">The following illustration shows a frame that contains an instance of a protocol.</span></span>

![um quadro que contém uma instância de protocolo](images/parser1.png)

<span data-ttu-id="6ad23-116">Se Monitor de Rede for exibir dados analisados na interface do usuário, o analisador deverá formatar os dados.</span><span class="sxs-lookup"><span data-stu-id="6ad23-116">If Network Monitor is going to display parsed data in the UI, the parser must format the data.</span></span> <span data-ttu-id="6ad23-117">No entanto, alguns especialistas usam a saída do analisador programaticamente e não exibem a saída na interface do usuário do Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="6ad23-117">However, some experts use the parser output programmatically, and do not display the output in the Network Monitor UI.</span></span> <span data-ttu-id="6ad23-118">Os dados exibidos incluem dados definidos pelo analisador e os dados na captura.</span><span class="sxs-lookup"><span data-stu-id="6ad23-118">Displayed data includes both parser-defined data, and the data in the capture.</span></span> <span data-ttu-id="6ad23-119">Por exemplo, o analisador normalmente fornece um nome para uma propriedade que é exibida e os dados na captura que está associado à propriedade.</span><span class="sxs-lookup"><span data-stu-id="6ad23-119">For example, the parser typically provides both a name for a property that is displayed, and the data in the capture that is associated with the property.</span></span>



| <span data-ttu-id="6ad23-120">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="6ad23-120">For information about</span></span>                                         | <span data-ttu-id="6ad23-121">Consulte</span><span class="sxs-lookup"><span data-stu-id="6ad23-121">See</span></span>                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6ad23-122">Quais pontos de entrada devem ser implementados dentro da DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="6ad23-122">Which entry points must be implemented within the parser DLL.</span></span> | [<span data-ttu-id="6ad23-123">Arquitetura de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="6ad23-123">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                 |
| <span data-ttu-id="6ad23-124">Como implementar funções de exportação de DLL do parser.</span><span class="sxs-lookup"><span data-stu-id="6ad23-124">How to implement parser DLL export functions.</span></span>                 | [<span data-ttu-id="6ad23-125">Gravando um analisador de protocolo</span><span class="sxs-lookup"><span data-stu-id="6ad23-125">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="6ad23-126">Quais analisadores de funções e estruturas usam.</span><span class="sxs-lookup"><span data-stu-id="6ad23-126">Which functions and structures parsers use.</span></span>                   | [<span data-ttu-id="6ad23-127">Funções e estruturas do analisador</span><span class="sxs-lookup"><span data-stu-id="6ad23-127">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



