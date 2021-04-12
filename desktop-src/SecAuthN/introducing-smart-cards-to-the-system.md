---
description: Antes que o subsistema de cartão inteligente possa encontrar um cartão inteligente, o cartão inteligente deve ser introduzido no sistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Introdução de cartões inteligentes ao sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171254"
---
# <a name="introducing-smart-cards-to-the-system"></a><span data-ttu-id="00152-103">Introdução de cartões inteligentes ao sistema</span><span class="sxs-lookup"><span data-stu-id="00152-103">Introducing Smart Cards to the System</span></span>

<span data-ttu-id="00152-104">Antes que o [*subsistema de cartão inteligente*](../secgloss/s-gly.md) possa encontrar um [*cartão inteligente*](../secgloss/s-gly.md), o cartão inteligente deve ser introduzido no sistema.</span><span class="sxs-lookup"><span data-stu-id="00152-104">Before the [*smart card subsystem*](../secgloss/s-gly.md) can find a [*smart card*](../secgloss/s-gly.md), the smart card must be introduced to the system.</span></span> <span data-ttu-id="00152-105">Isso normalmente é feito com uma ferramenta de configuração de cartão inteligente fornecida pelo fabricante do cartão.</span><span class="sxs-lookup"><span data-stu-id="00152-105">This is typically done with a smart card setup tool provided by the card manufacturer.</span></span> <span data-ttu-id="00152-106">A ferramenta pode ser um programa em um disquete (com o cartão inteligente), um controle ActiveX disponível em um site e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="00152-106">The tool could come as a program on a floppy disk (with the smart card), an ActiveX control available on a website, and so on.</span></span>

<span data-ttu-id="00152-107">A ferramenta de instalação deve fornecer as seguintes informações sobre o cartão:</span><span class="sxs-lookup"><span data-stu-id="00152-107">The setup tool must provide the following pieces of information about the card:</span></span>

-   <span data-ttu-id="00152-108">Sua [*cadeia de caracteres ATR*](../secgloss/a-gly.md)e uma máscara opcional para usar como uma ajuda na identificação do cartão.</span><span class="sxs-lookup"><span data-stu-id="00152-108">Its [*ATR string*](../secgloss/a-gly.md), and an optional mask to use as an aid in identifying the card.</span></span>
-   <span data-ttu-id="00152-109">Uma lista de interfaces de cartão inteligente com suporte no cartão.</span><span class="sxs-lookup"><span data-stu-id="00152-109">A list of smart card interfaces supported by the card.</span></span>
-   <span data-ttu-id="00152-110">Um nome de exibição para o cartão a ser usado na identificação do cartão para o usuário.</span><span class="sxs-lookup"><span data-stu-id="00152-110">A display name for the card, to be used in identifying the card to the user.</span></span> <span data-ttu-id="00152-111">Na maioria dos casos, o usuário fornecerá isso à ferramenta de instalação.</span><span class="sxs-lookup"><span data-stu-id="00152-111">In most cases, the user will supply this to the setup tool.</span></span>
-   <span data-ttu-id="00152-112">O [*provedor de serviços primário*](../secgloss/p-gly.md) associado ao cartão (opcional) a ser usado ao acessar o cartão por meio de interfaces com.</span><span class="sxs-lookup"><span data-stu-id="00152-112">The [*primary service provider*](../secgloss/p-gly.md) associated with the card (optional), to be used when accessing the card through COM interfaces.</span></span>

<span data-ttu-id="00152-113">Para simplificar as ferramentas de instalação e garantir a integridade do [*banco de dados do cartão inteligente*](../secgloss/s-gly.md), o subsistema de cartão inteligente fornece as duas funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="00152-113">To simplify setup tools, and to ensure the integrity of the [*smart card database*](../secgloss/s-gly.md), the smart card subsystem provides the following two functions.</span></span> <span data-ttu-id="00152-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduz um cartão inteligente no banco de dados e o [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) o Remove do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="00152-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduces a smart card into the database and [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) removes it from the database.</span></span>

 

 
