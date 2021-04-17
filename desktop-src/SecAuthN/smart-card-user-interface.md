---
description: A interface do usuário do cartão inteligente (IU) é uma única caixa de diálogo comum que permite que o usuário especifique ou procure um cartão inteligente para abrir (ou seja, conectar-se e usar em um aplicativo).
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Interface do usuário do cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751086"
---
# <a name="smart-card-user-interface"></a><span data-ttu-id="43e42-103">Interface do usuário do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="43e42-103">Smart Card User Interface</span></span>

<span data-ttu-id="43e42-104">A interface do [*usuário*](../secgloss/u-gly.md) do cartão inteligente (IU) é uma única [*caixa de diálogo comum*](../secgloss/s-gly.md) que permite que o usuário especifique ou procure um cartão inteligente para abrir (ou seja, conectar-se e usar em um aplicativo).</span><span class="sxs-lookup"><span data-stu-id="43e42-104">The smart card [*user interface*](../secgloss/u-gly.md) (UI) is a single [*common dialog box*](../secgloss/s-gly.md) that lets the user specify or search for a smart card to open (that is, connect to and use in an application).</span></span>

<span data-ttu-id="43e42-105">A seguir, há duas maneiras de usar a caixa de diálogo comum.</span><span class="sxs-lookup"><span data-stu-id="43e42-105">Following are two ways you can use the common dialog box.</span></span> <span data-ttu-id="43e42-106">Ambos supõem que a interface do usuário da caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="43e42-106">Both assume that the dialog box UI will be displayed.</span></span> <span data-ttu-id="43e42-107">Para obter mais informações, consulte [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span><span class="sxs-lookup"><span data-stu-id="43e42-107">For more information, see [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).</span></span>

<span data-ttu-id="43e42-108">**Para selecionar um cartão inteligente para abrir**</span><span class="sxs-lookup"><span data-stu-id="43e42-108">**To select a smart card to open**</span></span>

1.  <span data-ttu-id="43e42-109">Declare uma variável do tipo **OPENCARDNAME**.</span><span class="sxs-lookup"><span data-stu-id="43e42-109">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="43e42-110">Forneça informações suficientes na caixa de diálogo comum para restringir a pesquisa de um cartão inteligente que o aplicativo de chamada está procurando.</span><span class="sxs-lookup"><span data-stu-id="43e42-110">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="43e42-111">Isso inclui a especificação de **lpstrGroupNames**, **lpstrCardNames** e **rgguidInterfaces**.</span><span class="sxs-lookup"><span data-stu-id="43e42-111">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span> <span data-ttu-id="43e42-112">Isso também inclui a especificação de um modo de compartilhamento preferencial e o protocolo a ser usado quando a caixa de diálogo comum se conecta ao cartão usando os membros **dwShareMode** e **DwPreferredProtocols** da estrutura [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) .</span><span class="sxs-lookup"><span data-stu-id="43e42-112">This also includes specifying a preferred share mode and protocol to use when the common dialog box connects to the card by using the **dwShareMode** and **dwPreferredProtocols** members of the [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) structure.</span></span>
3.  <span data-ttu-id="43e42-113">Chame a função [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) para exibir a caixa de diálogo comum para o usuário.</span><span class="sxs-lookup"><span data-stu-id="43e42-113">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) function to display the common dialog box to the user.</span></span> <span data-ttu-id="43e42-114">Uma linha de informações de ajuda simples será exibida e, se um dos cartões que estão sendo solicitados for encontrado, o cartão será realçado na exibição.</span><span class="sxs-lookup"><span data-stu-id="43e42-114">A simple help information line will be displayed, and if one of the cards being requested is found, the card will be highlighted in the display.</span></span> <span data-ttu-id="43e42-115">Para pesquisas de nome de cartão múltiplo, o primeiro leitor que contém um dos cartões preferenciais será realçado.</span><span class="sxs-lookup"><span data-stu-id="43e42-115">For multiple card name searches, the first reader that contains one of the preferred cards will be highlighted.</span></span>
4.  <span data-ttu-id="43e42-116">Em seguida, o usuário seleciona um cartão, clica em **OK** e se conecta ao cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="43e42-116">The user then selects a card, clicks **OK**, and connects to the smart card.</span></span>

<span data-ttu-id="43e42-117">**Para procurar um cartão específico**</span><span class="sxs-lookup"><span data-stu-id="43e42-117">**To search for a specific card**</span></span>

1.  <span data-ttu-id="43e42-118">Declare uma variável do tipo **OPENCARDNAME**.</span><span class="sxs-lookup"><span data-stu-id="43e42-118">Declare a variable of type **OPENCARDNAME**.</span></span>
2.  <span data-ttu-id="43e42-119">Forneça informações suficientes na caixa de diálogo comum para restringir a pesquisa de um cartão inteligente que o aplicativo de chamada está procurando.</span><span class="sxs-lookup"><span data-stu-id="43e42-119">Provide enough information in the common dialog box to narrow the search for a smart card that the calling application is looking for.</span></span> <span data-ttu-id="43e42-120">Isso inclui a especificação de **lpstrGroupNames**, **lpstrCardNames** e **rgguidInterfaces**.</span><span class="sxs-lookup"><span data-stu-id="43e42-120">This includes specifying **lpstrGroupNames**, **lpstrCardNames**, and **rgguidInterfaces**.</span></span>
3.  <span data-ttu-id="43e42-121">Crie as funções de retorno de chamada **conectar**, **verificar** e **Desconectar** e defina os membros de dados **lpfnConnect**, **lpfnCheck** e **lpfnDisconnect** adequadamente.</span><span class="sxs-lookup"><span data-stu-id="43e42-121">Create the **Connect**, **Check**, and **Disconnect** callback functions, and set the **lpfnConnect**, **lpfnCheck**, and **lpfnDisconnect** data members appropriately.</span></span>
    > [!Note]  
    > <span data-ttu-id="43e42-122">Todas as três funções e membros devem estar disponíveis ao usar a caixa de diálogo comum dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="43e42-122">All three functions and members must be available when using the common dialog box in this way.</span></span>

     

4.  <span data-ttu-id="43e42-123">Chame a função de caixa de diálogo [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) comum.</span><span class="sxs-lookup"><span data-stu-id="43e42-123">Call the [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) common dialog box function.</span></span>
5.  <span data-ttu-id="43e42-124">A caixa de diálogo comum irá procurar os cartões solicitados.</span><span class="sxs-lookup"><span data-stu-id="43e42-124">The common dialog box will then search for the requested cards.</span></span> <span data-ttu-id="43e42-125">Se uma [*cadeia de caracteres ATR*](../secgloss/a-gly.md) ou nome do cartão de correspondência for encontrada, as funções de retorno de chamada **conectar**, **verificar** e **Desconectar** serão chamadas em sequência.</span><span class="sxs-lookup"><span data-stu-id="43e42-125">If a matching card name or [*ATR string*](../secgloss/a-gly.md) is found, the **Connect**, **Check**, and **Disconnect** callback functions will be called in sequence.</span></span> <span data-ttu-id="43e42-126">Se um cartão passar a rotina de **verificação** (ou seja, o retorno de chamada de **verificação** retornar **true**), esse cartão será realçado na exibição para o usuário.</span><span class="sxs-lookup"><span data-stu-id="43e42-126">If a card passes the **Check** routine (that is, the **Check** callback returns **TRUE**), this card is highlighted in the display to the user.</span></span>
    > [!Note]  
    > <span data-ttu-id="43e42-127">Se vários nomes de cartão forem fornecidos, o primeiro leitor que contém um dos cartões solicitados e passará a rotina de **verificação** será o cartão selecionado.</span><span class="sxs-lookup"><span data-stu-id="43e42-127">If multiple card names are given, the first reader that contains one of the requested cards and passes the **Check** routine will be the selected card.</span></span>

     

6.  <span data-ttu-id="43e42-128">Se nenhuma correspondência for encontrada, uma caixa de diálogo comum será exibida.</span><span class="sxs-lookup"><span data-stu-id="43e42-128">If no matches are found, a common dialog box will appear.</span></span>

 

 
