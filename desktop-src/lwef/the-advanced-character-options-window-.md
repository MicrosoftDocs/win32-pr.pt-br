---
title: Janela Opções avançadas de caractere (janela Comandos de Voz)
description: Saiba mais sobre a Janela Opções Avançadas de Caracteres, que fornece opções para os usuários ajustarem sua interação com todos os caracteres.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404350"
---
# <a name="advanced-character-options-window-voice-commands-window"></a><span data-ttu-id="a86cc-103">Janela Opções avançadas de caractere (janela Comandos de Voz)</span><span class="sxs-lookup"><span data-stu-id="a86cc-103">Advanced Character Options Window (Voice Commands Window)</span></span>

<span data-ttu-id="a86cc-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a86cc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="a86cc-105">A janela Opções avançadas de caractere fornece opções para que os usuários ajustem sua interação com todos os caracteres.</span><span class="sxs-lookup"><span data-stu-id="a86cc-105">The Advanced Character Options window provides options for users to adjust their interaction with all characters.</span></span> <span data-ttu-id="a86cc-106">Por exemplo, os usuários podem desabilitar a entrada de fala ou alterar parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="a86cc-106">For example, users can disable speech input or change input parameters.</span></span> <span data-ttu-id="a86cc-107">Os usuários também podem alterar as configurações de saída para a palavra balão.</span><span class="sxs-lookup"><span data-stu-id="a86cc-107">Users can also change the output settings for the word balloon.</span></span> <span data-ttu-id="a86cc-108">Essas configurações substituem qualquer conjunto por um aplicativo cliente ou definidos como parte da definição de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a86cc-108">These settings override any set by a client application or set as part of the character definition.</span></span> <span data-ttu-id="a86cc-109">Seu aplicativo não pode alterar nem desabilitar essas opções, pois elas se aplicam às preferências gerais do usuário para a operação de todos os caracteres.</span><span class="sxs-lookup"><span data-stu-id="a86cc-109">Your application cannot change or disable these options, because they apply to the general user preferences for operation of all characters.</span></span> <span data-ttu-id="a86cc-110">No entanto, o servidor notificará seu aplicativo ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) quando o usuário mudar e aplicar uma opção.</span><span class="sxs-lookup"><span data-stu-id="a86cc-110">However, the server will notify your application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) when the user changes and applies an option.</span></span> <span data-ttu-id="a86cc-111">Você também pode exibir ou fechar a janela usando a propriedade [**Visible**](visible-property.md) da janela e acessar seu local por meio de suas [**propriedades Superior**](top-property.md) [**e**](left-property.md) Esquerda.</span><span class="sxs-lookup"><span data-stu-id="a86cc-111">You can also display or close the window using the window's [**Visible**](visible-property.md) property and access its location through its [**Top**](top-property.md) and [**Left**](left-property.md) properties.</span></span>

<span data-ttu-id="a86cc-112">Além de dar suporte à animação de um caractere, o Microsoft Agent dá suporte à saída de áudio para o caractere.</span><span class="sxs-lookup"><span data-stu-id="a86cc-112">In addition to supporting the animation of a character, Microsoft Agent supports audio output for the character.</span></span> <span data-ttu-id="a86cc-113">Isso inclui a saída falada e efeitos de som.</span><span class="sxs-lookup"><span data-stu-id="a86cc-113">This includes spoken output and sound effects.</span></span> <span data-ttu-id="a86cc-114">Para a saída falada, o servidor sincroniza automaticamente as imagens de boca definidas do caractere com a saída.</span><span class="sxs-lookup"><span data-stu-id="a86cc-114">For spoken output, the server automatically lip-syncs the character's defined mouth images to the output.</span></span> <span data-ttu-id="a86cc-115">Você pode escolher a síntese de TTS (texto em fala), áudio gravado ou apenas saída de texto de balão de palavra.</span><span class="sxs-lookup"><span data-stu-id="a86cc-115">You can choose text-to-speech (TTS) synthesis, recorded audio, or only word balloon text output.</span></span>

 

 




