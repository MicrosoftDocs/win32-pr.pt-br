---
description: Trabalhando com menus de DVD
ms.assetid: 8c5f8072-b74f-4e15-8991-73bcc4145fd2
title: Trabalhando com menus de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113647a37200762b5eaf0a9ac231dea74ad19925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758044"
---
# <a name="working-with-dvd-menus"></a><span data-ttu-id="b7ef8-103">Trabalhando com menus de DVD</span><span class="sxs-lookup"><span data-stu-id="b7ef8-103">Working With DVD Menus</span></span>

<span data-ttu-id="b7ef8-104">O navegador de DVD pode mostrar um menu quando o usuário ativa um botão ou quando o navegador entra no primeiro domínio de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-104">The DVD Navigator might show a menu when the user activates a button, or when the Navigator enters the First Play domain.</span></span> <span data-ttu-id="b7ef8-105">Para mostrar um menu programaticamente, chame o método [**IDvdControl2:: domenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) .</span><span class="sxs-lookup"><span data-stu-id="b7ef8-105">To show a menu programmatically, call the [**IDvdControl2::ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu) method.</span></span>

<span data-ttu-id="b7ef8-106">Há várias maneiras de selecionar botões de menu programaticamente:</span><span class="sxs-lookup"><span data-stu-id="b7ef8-106">There are several ways to select menu buttons programmatically:</span></span>

-   <span data-ttu-id="b7ef8-107">Para selecionar um botão por número, chame [**IDvdControl2:: SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span><span class="sxs-lookup"><span data-stu-id="b7ef8-107">To select a button by number, call [**IDvdControl2::SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton).</span></span> <span data-ttu-id="b7ef8-108">Os botões são numerados de 1 a 36.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-108">Buttons are numbered 1 to 36.</span></span> <span data-ttu-id="b7ef8-109">O método [**IDvdInfo2:: GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) retorna o número de botões disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-109">The [**IDvdInfo2::GetCurrentButton**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentbutton) method returns the number of available buttons.</span></span>
-   <span data-ttu-id="b7ef8-110">Para selecionar um botão relativo à posição do botão atualmente selecionado, chame [**IDvdControl2:: SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span><span class="sxs-lookup"><span data-stu-id="b7ef8-110">To select a button relative to the position of the currently selected button, call [**IDvdControl2::SelectRelativeButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectrelativebutton).</span></span> <span data-ttu-id="b7ef8-111">Você pode selecionar um botão na direção para cima, para baixo, para a esquerda ou para a direita.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-111">You can select a button in the up, down, left, or right direction.</span></span>
-   <span data-ttu-id="b7ef8-112">Para selecionar um botão por suas coordenadas dentro da janela, chame [**IDvdControl2:: SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span><span class="sxs-lookup"><span data-stu-id="b7ef8-112">To select a button by its coordinates within the window, call [**IDvdControl2::SelectAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectatposition).</span></span> <span data-ttu-id="b7ef8-113">Esse método usa coordenadas (x, y) em relação à área do cliente da janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-113">This method takes (x,y) coordinates relative to the client area of the video window.</span></span> <span data-ttu-id="b7ef8-114">(Para o modo sem janela, essa é a janela do aplicativo.) Se não houver nenhum botão nesse local, o método retornará VFW \_ E \_ \_ nenhum botão de DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="b7ef8-114">(For windowless mode, this is the application window.) If there is no button at that location, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="b7ef8-115">Além disso, há várias maneiras de ativar um botão:</span><span class="sxs-lookup"><span data-stu-id="b7ef8-115">In addition, there are several ways to activate a button:</span></span>

-   <span data-ttu-id="b7ef8-116">Para ativar um botão por número, chame [**IDvdControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span><span class="sxs-lookup"><span data-stu-id="b7ef8-116">To activate a button by number, call [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton).</span></span>
-   <span data-ttu-id="b7ef8-117">Para ativar um botão por suas coordenadas, chame [**IDvdControl2:: ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span><span class="sxs-lookup"><span data-stu-id="b7ef8-117">To activate a button by its coordinates, call [**IDvdControl2::ActivateAtPosition**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activateatposition).</span></span>
-   <span data-ttu-id="b7ef8-118">Para ativar o botão que está selecionado no momento, chame [**IDvdControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span><span class="sxs-lookup"><span data-stu-id="b7ef8-118">To activate the button that is currently selected, call [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton).</span></span> <span data-ttu-id="b7ef8-119">Se nenhum botão for selecionado, o método retornará VFW \_ E \_ \_ nenhum botão de DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="b7ef8-119">If no button is selected, the method returns VFW\_E\_DVD\_NO\_BUTTON.</span></span>

<span data-ttu-id="b7ef8-120">Tenha em mente que a seleção de um botão simplesmente realça suas bordas.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-120">Keep in mind that selecting a button merely highlights its borders.</span></span> <span data-ttu-id="b7ef8-121">Para fazer com que o comando associado seja acionado, o botão deve ser ativado.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-121">To cause the associated command to be fired, the button must be activated.</span></span> <span data-ttu-id="b7ef8-122">A ativação de um botão programaticamente pode ser feita de várias maneiras, mas o botão sempre deve ser selecionado para que possa ser ativado.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-122">Activating a button programmatically can be done in various ways, but the button must always be selected before it can be activated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7ef8-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7ef8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7ef8-124">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="b7ef8-124">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



