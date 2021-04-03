---
title: Seleção do mecanismo de fala
description: Seleção do mecanismo de fala
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822549"
---
# <a name="speech-engine-selection"></a><span data-ttu-id="52d06-103">Seleção do mecanismo de fala</span><span class="sxs-lookup"><span data-stu-id="52d06-103">Speech Engine Selection</span></span>

<span data-ttu-id="52d06-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52d06-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="52d06-105">A configuração de ID de idioma de um caractere determina seu idioma de entrada de fala padrão; O Microsoft Agent solicita SAPI para um mecanismo instalado que corresponda a esse idioma.</span><span class="sxs-lookup"><span data-stu-id="52d06-105">A character's language ID setting determines its default speech input language; Microsoft Agent requests SAPI for an installed engine that matches that language.</span></span> <span data-ttu-id="52d06-106">Se um aplicativo cliente não especificar uma preferência de idioma, o Microsoft Agent tentará localizar um mecanismo de reconhecimento de fala que corresponda à ID de idioma padrão do usuário (usando a ID de idioma principal e, em seguida, a ID de idioma secundária).</span><span class="sxs-lookup"><span data-stu-id="52d06-106">If a client application does not specify a language preference, Microsoft Agent will attempt to find a speech recognition engine that matches the user default language ID (using the major language ID, then the minor language ID).</span></span> <span data-ttu-id="52d06-107">Se nenhum mecanismo estiver disponível correspondendo a esse idioma, a fala será desabilitada para esse caractere.</span><span class="sxs-lookup"><span data-stu-id="52d06-107">If no engine is available matching this language, speech is disabled for that character.</span></span>

<span data-ttu-id="52d06-108">Você também pode solicitar um mecanismo de reconhecimento de fala específico especificando sua ID de modo (usando a propriedade [**SRModeID**](srmodeid-property.md) de caracteres).</span><span class="sxs-lookup"><span data-stu-id="52d06-108">You can also request a specific speech recognition engine by specifying its mode ID (using the character [**SRModeID**](srmodeid-property.md) property).</span></span> <span data-ttu-id="52d06-109">No entanto, se a ID de idioma para essa ID de modo não corresponder à configuração de idioma do cliente, a chamada falhará (gerará um erro no controle).</span><span class="sxs-lookup"><span data-stu-id="52d06-109">However, if the language ID for that mode ID does not match the client's language setting, the call will fail (raise an error in the control).</span></span> <span data-ttu-id="52d06-110">O mecanismo de reconhecimento de fala permanecerá o último mecanismo definido com êxito pelo cliente, ou se nenhum, o mecanismo que corresponde à ID de idioma atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="52d06-110">The speech recognition engine will then remain the last successfully set engine by the client, or if none, the engine that matches the current system language ID.</span></span> <span data-ttu-id="52d06-111">Se ainda não houver correspondência, a entrada de fala não estará disponível para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="52d06-111">If there is still no match, speech input is not available for that client.</span></span>

<span data-ttu-id="52d06-112">O Microsoft Agent carrega automaticamente um mecanismo de reconhecimento de fala quando a entrada de fala é iniciada por um usuário pressionando a tecla de atalho de escuta ou o cliente de entrada-ativo chama o método [**Listen**](listen-method.md) .</span><span class="sxs-lookup"><span data-stu-id="52d06-112">Microsoft Agent automatically loads a speech recognition engine when speech input is initiated by a user pressing the Listening hotkey or the input-active client calls the [**Listen**](listen-method.md) method.</span></span> <span data-ttu-id="52d06-113">No entanto, um mecanismo também pode ser carregado ao definir ou consultar sua ID de modo, configurar ou consultar as propriedades da janela de comandos de voz, consultar [**SRStatus**](srstatus-property.md)ou quando a fala estiver habilitada e o usuário exibir a página de entrada de fala das opções de caractere avançado.</span><span class="sxs-lookup"><span data-stu-id="52d06-113">However, an engine may also be loaded when setting or querying its mode ID, setting or querying the properties of the Voice Commands Window, querying [**SRStatus**](srstatus-property.md), or when speech is enabled and the user displays the Speech Input page of the Advanced Character Options.</span></span> <span data-ttu-id="52d06-114">No entanto, o Microsoft Agent só mantém carregado os mecanismos de fala que os clientes estão usando.</span><span class="sxs-lookup"><span data-stu-id="52d06-114">However, Microsoft Agent only keeps loaded the speech engines that clients are using.</span></span>

 

 




