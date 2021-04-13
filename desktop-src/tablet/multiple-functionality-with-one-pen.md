---
description: Uma caneta do Tablet PC pode ter mais de uma extremidade que possa interagir com o digitalizador.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Várias funcionalidades com uma caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297625"
---
# <a name="multiple-functionality-with-one-pen"></a><span data-ttu-id="1f9d6-103">Várias funcionalidades com uma caneta</span><span class="sxs-lookup"><span data-stu-id="1f9d6-103">Multiple Functionality with One Pen</span></span>

<span data-ttu-id="1f9d6-104">Uma caneta do Tablet PC pode ter mais de uma extremidade que possa interagir com o digitalizador.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-104">A Tablet PC pen may have more than one end that can interact with the digitizer.</span></span> <span data-ttu-id="1f9d6-105">Se ambas as extremidades da caneta puderem gerar eventos, uma extremidade poderá ser usada para definir a tinta, selecionar e apontar, e a outra extremidade poderá ser usada para outras funções, como apagar.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-105">If both ends of the pen can generate events, one end may be used to lay down ink, select, and point, and the other end may be used for other functions such as erasing.</span></span>

<span data-ttu-id="1f9d6-106">Para implementar essa funcionalidade, seu aplicativo deve ser capaz de determinar qual extremidade da caneta está sendo usada e, portanto, quando alterar a aparência do cursor.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-106">To implement such functionality, your application must be able to determine which end of the pen is being used and hence when to change the appearance of the cursor.</span></span> <span data-ttu-id="1f9d6-107">Isso pode fazer isso procurando o estado da propriedade [**invertida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) no objeto [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="1f9d6-107">It can do this by looking for the state of the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

<span data-ttu-id="1f9d6-108">Para obter detalhes específicos sobre como usar a parte traseira da caneta para apagar, consulte [apagando a tinta com a caneta](erasing-ink-with-the-pen.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d6-108">For specific details about using the back of the pen for erasing, see [Erasing Ink with the Pen](erasing-ink-with-the-pen.md).</span></span> <span data-ttu-id="1f9d6-109">Além disso, o [exemplo de apagamento de tinta](ink-erasing-sample.md) demonstra como usar a parte traseira da caneta para apagar a tinta.</span><span class="sxs-lookup"><span data-stu-id="1f9d6-109">In addition, the [Ink Erasing Sample](ink-erasing-sample.md) demonstrates how to use the back of the pen to erase ink.</span></span>

 

 



