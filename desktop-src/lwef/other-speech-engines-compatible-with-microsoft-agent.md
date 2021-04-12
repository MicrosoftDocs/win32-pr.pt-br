---
title: Outros mecanismos de fala compatíveis com o Microsoft Agent
description: Outros mecanismos de fala compatíveis com o Microsoft Agent
ms.assetid: fa87c592-c819-4dea-a1d0-6ccb25cc0bcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9855a0f5374d35634d02f808b46449a053cada9a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365657"
---
# <a name="other-speech-engines-compatible-with-microsoft-agent"></a><span data-ttu-id="e3e21-103">Outros mecanismos de fala compatíveis com o Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="e3e21-103">Other Speech Engines Compatible with Microsoft Agent</span></span>

<span data-ttu-id="e3e21-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3e21-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e3e21-105">Além dos mecanismos de fala da Microsoft que são fornecidos com o e dão suporte ao Microsoft Agent, várias empresas também oferecem mecanismos de fala com suporte para o Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e3e21-105">In addition to the Microsoft speech engines that are provided with and support Microsoft Agent, a number of companies also offer speech engines with support for Microsoft Agent.</span></span> <span data-ttu-id="e3e21-106">Esta página fornece uma breve visão geral de tais mecanismos que podem estar disponíveis no inglês dos EUA e em outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="e3e21-106">This page gives you a brief overview of such engines that may be available in U.S. English and other languages.</span></span> <span data-ttu-id="e3e21-107">Informações sobre como instalar e acessar, bem como licenciar e redistribuir os mecanismos, podem ser encontradas em seus sites.</span><span class="sxs-lookup"><span data-stu-id="e3e21-107">Information about how to install and access, as well as license and redistribute the engines can be found at their websites.</span></span>

<span data-ttu-id="e3e21-108">Ao usar qualquer mecanismo de fala de terceiros, você também precisa instalar os binários do Microsoft SAPI 4.0 em tempo de execução para que os mecanismos sejam enumerados corretamente.</span><span class="sxs-lookup"><span data-stu-id="e3e21-108">When using any third-party speech engine, you also need to install Microsoft SAPI 4.0a runtime binaries so that the engines are enumerated properly.</span></span> <span data-ttu-id="e3e21-109">Na página da Web, você pode incluir a seguinte marcação para disparar um download automotivo do Speech API:</span><span class="sxs-lookup"><span data-stu-id="e3e21-109">From your webpage you can include the following tag to trigger an autodownload of the Speech API:</span></span>

``` syntax
<OBJECT WIDTH=0 HEIGHT=0
  CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
  CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

<span data-ttu-id="e3e21-110">Para obter mais informações sobre os binários de tempo de execução SAPI, consulte o [site do grupo de fala da Microsoft](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3e21-110">For more information about the SAPI runtime binaries, refer to the [Microsoft Speech group's website](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="e3e21-111">O Microsoft Agent também instala os binários de tempo de execução SAPI com o mecanismo de reconhecimento de fala da Microsoft, o painel de controle de fala e o editor de caracteres do agente.</span><span class="sxs-lookup"><span data-stu-id="e3e21-111">Microsoft Agent also installs the SAPI runtime binaries with the Microsoft Speech Recognition Engine, the Speech Control Panel, and the Agent Character Editor.</span></span>

<span data-ttu-id="e3e21-112">Observe que esses links apontam para servidores que não estão sob o controle da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e3e21-112">Please note that these links point to servers that are not under Microsoft control.</span></span> <span data-ttu-id="e3e21-113">Leia a [declaração oficial](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) da Microsoft sobre outros servidores.</span><span class="sxs-lookup"><span data-stu-id="e3e21-113">Please read the Microsoft [official statement](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) regarding other servers.</span></span> <span data-ttu-id="e3e21-114">A Microsoft não endossa o conteúdo nem o software fornecido nesses sites.</span><span class="sxs-lookup"><span data-stu-id="e3e21-114">Microsoft does not endorse the content nor the software provided at these websites.</span></span> <span data-ttu-id="e3e21-115">Todas as perguntas técnicas e de suporte também devem ser direcionadas aos fornecedores dos mecanismos e não à Microsoft ou à equipe do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e3e21-115">All technical and support questions should also be directed to the suppliers of the engines and not to Microsoft or the Microsoft Agent team.</span></span>

<span data-ttu-id="e3e21-116">**Mecanismo de conversão de texto em fala do Digalo**</span><span class="sxs-lookup"><span data-stu-id="e3e21-116">**Digalo Text-To-Speech Engine**</span></span>

<span data-ttu-id="e3e21-117">Digalo é um mecanismo de TTS econômico projetado para usuários finais e desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="e3e21-117">Digalo is an affordable TTS engine designed for end-users and developers.</span></span> <span data-ttu-id="e3e21-118">O mecanismo é oferecido em várias linguagens: francês, alemão, Português (Brasil), espanhol, russo e Reino Unido e inglês americano, com italiano, polonês e outras linguagens em breve.</span><span class="sxs-lookup"><span data-stu-id="e3e21-118">The engine is offered in a number of languages: French, German, Portuguese (Brazil), Spanish, Russian, and UK and U.S. English, with Italian, Polish, and other languages coming soon.</span></span> <span data-ttu-id="e3e21-119">As informações do desenvolvedor, bem como detalhes sobre o registro do usuário final e os programas afiliados, também estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e3e21-119">Developer information, as well as details on end-user registration and affiliate programs, is also available.</span></span>

<span data-ttu-id="e3e21-120">**Mecanismo de fala Elan**</span><span class="sxs-lookup"><span data-stu-id="e3e21-120">**Elan Speech Engine**</span></span>

<span data-ttu-id="e3e21-121">O mecanismo de fala Elan usa a tecnologia de texto para fala da Elan e está disponível em sete idiomas: francês, alemão, Português (Brasil), espanhol, russo, Reino Unido e inglês americano.</span><span class="sxs-lookup"><span data-stu-id="e3e21-121">Elan Speech Engine uses Elan's Text To Speech technology and is available in seven languages: French, German, Portuguese (Brazil), Spanish, Russian, UK and U.S. English.</span></span>

<span data-ttu-id="e3e21-122">**IBM ViaVoice muito alto**</span><span class="sxs-lookup"><span data-stu-id="e3e21-122">**IBM ViaVoice Outloud**</span></span>

<span data-ttu-id="e3e21-123">A IBM desenvolveu vários caracteres do Microsoft Agent para uso com ViaVoice de baixo.</span><span class="sxs-lookup"><span data-stu-id="e3e21-123">IBM has developed several Microsoft Agent characters for use with ViaVoice Outloud.</span></span> <span data-ttu-id="e3e21-124">O IBM ViaVoice com alta disponibilidade é uma tecnologia de texto para fala (síntese de fala) e está disponível em francês, alemão, italiano, espanhol, Reino Unido e inglês dos EUA.</span><span class="sxs-lookup"><span data-stu-id="e3e21-124">IBM ViaVoice Outloud is a text-to-speech (speech synthesis) technology and is available in French, German, Italian, Spanish, UK English and U.S. English.</span></span> <span data-ttu-id="e3e21-125">Quando combinado com o Microsoft Agent, você pode criar aplicativos vibrantes em várias linguagens e estender suas oportunidades de vendas para novos mercados mundiais.</span><span class="sxs-lookup"><span data-stu-id="e3e21-125">When combined with Microsoft Agent, you can create vibrant applications in many languages and extend your sales opportunities to new worldwide markets.</span></span>

 

 




