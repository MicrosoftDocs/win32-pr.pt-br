---
title: O objeto CommandsWindow
description: O objeto CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105791379"
---
# <a name="the-commandswindow-object"></a><span data-ttu-id="5f93d-103">O objeto CommandsWindow</span><span class="sxs-lookup"><span data-stu-id="5f93d-103">The CommandsWindow Object</span></span>

<span data-ttu-id="5f93d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f93d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="5f93d-105">O objeto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) fornece acesso às propriedades da janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="5f93d-105">The [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) object provides access to properties of the Voice Commands Window.</span></span> <span data-ttu-id="5f93d-106">A janela de comandos de voz é um recurso compartilhado projetado principalmente para permitir que os usuários exibam comandos habilitados para voz.</span><span class="sxs-lookup"><span data-stu-id="5f93d-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="5f93d-107">Se o reconhecimento de fala estiver desabilitado, a janela comandos de voz ainda será exibida, com o texto "entrada de fala desabilitada" (no idioma do caractere).</span><span class="sxs-lookup"><span data-stu-id="5f93d-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="5f93d-108">Se não houver nenhum mecanismo de fala instalado que corresponda à configuração de idioma do caractere, a janela será exibida, "entrada de fala não disponível".</span><span class="sxs-lookup"><span data-stu-id="5f93d-108">If no speech engine is installed that matches the character's language setting the window displays, "Speech input not available."</span></span> <span data-ttu-id="5f93d-109">Se o cliente de entrada-ativo não tiver definido parâmetros de voz para seus comandos e tiver desabilitado os comandos de voz globais, a janela exibirá "nenhum comando de voz".</span><span class="sxs-lookup"><span data-stu-id="5f93d-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="5f93d-110">Você também pode consultar as propriedades da janela de comandos de voz independentemente se a entrada de fala está desabilitada ou se um mecanismo de fala compatível está instalado.</span><span class="sxs-lookup"><span data-stu-id="5f93d-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

-   [<span data-ttu-id="5f93d-111">Propriedades de CommandsWindow</span><span class="sxs-lookup"><span data-stu-id="5f93d-111">CommandsWindow Properties</span></span>](commandswindow-properties.md)

 

 