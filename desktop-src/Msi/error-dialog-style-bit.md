---
description: Se esse bit for definido, a caixa de diálogo será um diálogo de erro.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit de estilo de caixa de diálogo de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748594"
---
# <a name="error-dialog-style-bit"></a><span data-ttu-id="89181-103">Bit de estilo de caixa de diálogo de erro</span><span class="sxs-lookup"><span data-stu-id="89181-103">Error Dialog Style Bit</span></span>

<span data-ttu-id="89181-104">Se esse bit for definido, a caixa de diálogo será um diálogo de erro.</span><span class="sxs-lookup"><span data-stu-id="89181-104">If this bit is set, the dialog box is an error dialog.</span></span>

<span data-ttu-id="89181-105">Pode haver mais de uma caixa de diálogo com este estilo.</span><span class="sxs-lookup"><span data-stu-id="89181-105">There can be more than one dialog with this style.</span></span> <span data-ttu-id="89181-106">A propriedade **ErrorDialog** determina qual caixa de diálogo é usada como uma caixa de diálogo de erro.</span><span class="sxs-lookup"><span data-stu-id="89181-106">The **ErrorDialog** property determines which dialog is used as an error dialog.</span></span> <span data-ttu-id="89181-107">A caixa de diálogo selecionada pode ser apenas uma das que têm esse conjunto de bits de estilo.</span><span class="sxs-lookup"><span data-stu-id="89181-107">The selected dialog can be only one of those that have this style bit set.</span></span> <span data-ttu-id="89181-108">A caixa de diálogo de erro deve ter um controle de texto estático chamado ErrorText.</span><span class="sxs-lookup"><span data-stu-id="89181-108">The error dialog must have a static text control named ErrorText.</span></span> <span data-ttu-id="89181-109">Esse controle recebe o texto da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="89181-109">This control receives the text of the error message.</span></span> <span data-ttu-id="89181-110">A caixa de diálogo também deve ter os sete botões de push correspondentes aos possíveis valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="89181-110">The dialog should also have the seven push buttons corresponding to the possible return values.</span></span> <span data-ttu-id="89181-111">A mensagem de erro determina quais desses botões são realmente exibidos.</span><span class="sxs-lookup"><span data-stu-id="89181-111">The error message determines which of these buttons are actually displayed.</span></span> <span data-ttu-id="89181-112">Os botões exibidos são reorganizados para que sejam distribuídos uniformemente na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89181-112">The displayed buttons are rearranged so they are evenly distributed on the dialog.</span></span> <span data-ttu-id="89181-113">Essa reorganização altera a coordenada X dos botões, mas não as outras três coordenadas.</span><span class="sxs-lookup"><span data-stu-id="89181-113">This rearrangement changes the X coordinate of the buttons, but not the other three coordinates.</span></span> <span data-ttu-id="89181-114">Portanto, é aconselhável que nenhum outro controle seja criado na mesma região horizontal da caixa de diálogo que os botões.</span><span class="sxs-lookup"><span data-stu-id="89181-114">Therefore it is advisable that no other control should be authored in the same horizontal region of the dialog as the buttons.</span></span> <span data-ttu-id="89181-115">Se a mensagem de erro não especificar nenhum botão, o botão **OK** será exibido.</span><span class="sxs-lookup"><span data-stu-id="89181-115">If the error message specifies no button, the **OK** button is displayed.</span></span> <span data-ttu-id="89181-116">O botão **padrão** , o primeiro controle ativo e os valores de botão de **cancelamento** são ignorados para uma caixa de diálogo de erro.</span><span class="sxs-lookup"><span data-stu-id="89181-116">The **Default** button, First active control and **Cancel** button values are ignored for an error dialog.</span></span> <span data-ttu-id="89181-117">O botão **padrão** definido na mensagem de erro será atribuído a todos os três valores.</span><span class="sxs-lookup"><span data-stu-id="89181-117">The **Default** button defined in the error message will be assigned to all three values.</span></span> <span data-ttu-id="89181-118">O efeito de enviar esses botões deve ser definido na [tabela ControlEvent,](controlevent-table.md) , assim como para todos os outros botões.</span><span class="sxs-lookup"><span data-stu-id="89181-118">The effect of pushing these buttons have to be defined in the [ControlEvent table](controlevent-table.md) just like for all other buttons.</span></span> <span data-ttu-id="89181-119">O título da caixa de diálogo é criado de forma semelhante a outras caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="89181-119">The title of the dialog is authored in a way similar to other dialogs.</span></span> <span data-ttu-id="89181-120">Ele poderá ser substituído pela mensagem de erro se especificar um texto de cabeçalho após a lista de botões.</span><span class="sxs-lookup"><span data-stu-id="89181-120">It can get overwritten by the error message if it specifies a header text after the button list.</span></span>

## <a name="value"></a><span data-ttu-id="89181-121">Valor</span><span class="sxs-lookup"><span data-stu-id="89181-121">Value</span></span>



| <span data-ttu-id="89181-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="89181-122">Decimal</span></span> | <span data-ttu-id="89181-123">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="89181-123">Hexadecimal</span></span> | <span data-ttu-id="89181-124">Constante</span><span class="sxs-lookup"><span data-stu-id="89181-124">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="89181-125">65536</span><span class="sxs-lookup"><span data-stu-id="89181-125">65536</span></span>   | <span data-ttu-id="89181-126">0x00010000</span><span class="sxs-lookup"><span data-stu-id="89181-126">0x00010000</span></span>  | <span data-ttu-id="89181-127">**msidbDialogAttributesError**</span><span class="sxs-lookup"><span data-stu-id="89181-127">**msidbDialogAttributesError**</span></span> |



 

 

 



