---
title: A janela de caracteres
description: A janela de caracteres
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368963"
---
# <a name="the-character-window"></a><span data-ttu-id="511c8-103">A janela de caracteres</span><span class="sxs-lookup"><span data-stu-id="511c8-103">The Character Window</span></span>

<span data-ttu-id="511c8-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="511c8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="511c8-105">O Microsoft Agent exibe caracteres animados em suas próprias janelas que sempre aparecem na parte superior da ordem z da janela (ou seja, always on Top).</span><span class="sxs-lookup"><span data-stu-id="511c8-105">Microsoft Agent displays animated characters in their own windows that always appear at the top of the window z-order (that is, always on top).</span></span> <span data-ttu-id="511c8-106">Um usuário pode mover a janela de um caractere arrastando o caractere com o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="511c8-106">A user can move a character's window by dragging the character with the left mouse button.</span></span> <span data-ttu-id="511c8-107">A imagem de caractere é movida com o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="511c8-107">The character image moves with the pointer.</span></span> <span data-ttu-id="511c8-108">Além disso, um aplicativo pode mover um caractere usando o método [**MoveTo**](moveto-method.md) .</span><span class="sxs-lookup"><span data-stu-id="511c8-108">In addition, an application can move a character using the [**MoveTo**](moveto-method.md) method.</span></span>

<span data-ttu-id="511c8-109">Quando o usuário clica com o botão direito do mouse em um caractere, é exibido um menu pop-up que exibe os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="511c8-109">When the user right-clicks a character, a pop-up menu appears that displays the following commands:</span></span>

<span data-ttu-id="511c8-110">Abrir \| fechar a janela de comandos do <span class="underline">V</span>Assis</span><span class="sxs-lookup"><span data-stu-id="511c8-110">Open \| Close <span class="underline">V</span>oice Commands Window</span></span>

<span data-ttu-id="511c8-111">IDE <span class="underline">H</span></span><span class="sxs-lookup"><span data-stu-id="511c8-111"><span class="underline">H</span>ide</span></span>

<span data-ttu-id="511c8-112">----------------------------…</span><span class="sxs-lookup"><span data-stu-id="511c8-112">----------------------------…</span></span>

<span data-ttu-id="511c8-113">Linha\*</span><span class="sxs-lookup"><span data-stu-id="511c8-113">Command\*</span></span>


<span data-ttu-id="511c8-114">*OtherHostingApplicationCaption\*\**</span><span class="sxs-lookup"><span data-stu-id="511c8-114">*OtherHostingApplicationCaption\*\**</span></span>

<span data-ttu-id="511c8-115">\*Os comandos listados são baseados no cliente de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="511c8-115">\*Commands listed are based on the input-active client.</span></span> <span data-ttu-id="511c8-116">Para obter mais informações sobre como definir comandos que aparecem no menu pop-up, consulte Visão geral da interface de programação do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="511c8-116">For more information on defining commands that appear in the pop-up menu, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="511c8-117">\*\*As entradas listadas são todos os outros aplicativos que estão hospedando o caractere no momento.</span><span class="sxs-lookup"><span data-stu-id="511c8-117">\*\*Entries listed are all other applications currently hosting the character.</span></span> <span data-ttu-id="511c8-118">Para obter mais informações sobre como definir essa entrada, consulte a visão geral da interface de programação do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="511c8-118">For more information on defining this entry, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="511c8-119">O \| comando abrir fechar voz comandos da janela controla a exibição da janela comandos do caractere ativo atual.</span><span class="sxs-lookup"><span data-stu-id="511c8-119">The Open \| Close Voice Commands Window command controls the display of the Commands Window of the current active character.</span></span> <span data-ttu-id="511c8-120">Se os serviços de reconhecimento de fala estiverem desabilitados, esse comando será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="511c8-120">If speech recognition services are disabled, this command is disabled.</span></span> <span data-ttu-id="511c8-121">Se os serviços de reconhecimento de fala não estiverem instalados, esse comando não será exibido.</span><span class="sxs-lookup"><span data-stu-id="511c8-121">If speech recognition services are not installed, this command does not appear.</span></span>

<span data-ttu-id="511c8-122">O comando Hide oculta o caractere.</span><span class="sxs-lookup"><span data-stu-id="511c8-122">The Hide command hides the character.</span></span> <span data-ttu-id="511c8-123">A animação atribuída ao estado de **ocultação** do caractere é reproduzida e oculta o caractere.</span><span class="sxs-lookup"><span data-stu-id="511c8-123">The animation assigned to the character's **Hiding** state plays and hides the character.</span></span> <span data-ttu-id="511c8-124">A letra "H" em Hide é a chave de acesso do comando (mnemônico).</span><span class="sxs-lookup"><span data-stu-id="511c8-124">The letter "H" in hide is the command's access key (mnemonic).</span></span>

<span data-ttu-id="511c8-125">Os comandos para os aplicativos que atualmente hospedam o caractere seguem o comando Hide, precedido por um separador.</span><span class="sxs-lookup"><span data-stu-id="511c8-125">The commands for the application(s) currently hosting the character follow the Hide command, preceded by a separator.</span></span> <span data-ttu-id="511c8-126">Em seguida, os nomes de outros aplicativos que usam o caractere são exibidos, também precedidos por um separador.</span><span class="sxs-lookup"><span data-stu-id="511c8-126">Then the names of other applications using the character appear, also preceded by a separator.</span></span>

 

 




