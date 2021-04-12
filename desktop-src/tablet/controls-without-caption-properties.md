---
description: Introdução ao uso de controles sem propriedades de legenda para o Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Controles sem propriedades de legenda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501132"
---
# <a name="controls-without-caption-properties"></a><span data-ttu-id="a8168-103">Controles sem propriedades de legenda</span><span class="sxs-lookup"><span data-stu-id="a8168-103">Controls Without Caption Properties</span></span>

<span data-ttu-id="a8168-104">Quando um controle não tiver sua própria propriedade Caption, execute as seguintes etapas para garantir que os auxílios de acessibilidade possam identificar os controles:</span><span class="sxs-lookup"><span data-stu-id="a8168-104">When a control does not have its own caption property, take the following steps to ensure that accessibility aids can identify the controls:</span></span>

-   <span data-ttu-id="a8168-105">Crie um controle de texto estático com um nome descritivo e significativo.</span><span class="sxs-lookup"><span data-stu-id="a8168-105">Create a static text control with a meaningful and descriptive name.</span></span>
-   <span data-ttu-id="a8168-106">Coloque o rótulo estático para que ele preceda imediatamente o controle referenciado, na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="a8168-106">Place the static label so it immediately precedes the referenced control, in tab order.</span></span>
-   <span data-ttu-id="a8168-107">Verifique se o texto do rótulo termina com dois-pontos, por exemplo, "configurações:"</span><span class="sxs-lookup"><span data-stu-id="a8168-107">Ensure that the label text ends with a colon, for example, "Settings:"</span></span>
-   <span data-ttu-id="a8168-108">Posicione o texto do rótulo imediatamente à esquerda ou antes do controle referenciado.</span><span class="sxs-lookup"><span data-stu-id="a8168-108">Position the label text immediately to the left or preceding the referenced control.</span></span>
-   <span data-ttu-id="a8168-109">Torne o texto estático invisível se não for apropriado exibi-lo visualmente.</span><span class="sxs-lookup"><span data-stu-id="a8168-109">Make the static text invisible if it is not appropriate to display it visually.</span></span> <span data-ttu-id="a8168-110">Faça isso atribuindo o atributo apropriado no script de recurso.</span><span class="sxs-lookup"><span data-stu-id="a8168-110">Do this by assigning the appropriate attribute in the resource script.</span></span> <span data-ttu-id="a8168-111">Isso pode ser apropriado quando o nome ou a função de um controle é fornecido visualmente por meio de um controle de texto estático, como um gráfico ou um botão de opção relacionado.</span><span class="sxs-lookup"><span data-stu-id="a8168-111">This may be appropriate when the name or function of a control is visually provided by means other than static text control, such as a graphic or a related radio button.</span></span>

<span data-ttu-id="a8168-112">O uso adequado de controles estáticos é a única maneira de implementar corretamente chaves de acesso de sublinhado para controles que não têm rótulos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="a8168-112">The proper use of static controls is the only way to correctly implement underlined access keys for controls that do not have intrinsic labels.</span></span> <span data-ttu-id="a8168-113">Para obter mais informações sobre como usar controles que não têm propriedades de legenda, consulte a seção [acessibilidade](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="a8168-113">For more information about using controls that do not have caption properties, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
