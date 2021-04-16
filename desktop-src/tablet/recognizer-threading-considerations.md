---
description: Embora um&\# 160; contexto de reconhecedor&\# 160; não possa ser acessado em dois threads simultaneamente pela plataforma do Tablet PC, a função AdviseInkChange pode ser chamada a qualquer momento em qualquer thread.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Considerações de Threading do reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765301"
---
# <a name="recognizer-threading-considerations"></a><span data-ttu-id="bfe46-103">Considerações de Threading do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="bfe46-103">Recognizer Threading Considerations</span></span>

<span data-ttu-id="bfe46-104">Embora um [contexto de reconhecedor](hrecocontext-handle.md) não possa ser acessado em dois threads simultaneamente pela plataforma do Tablet PC, a função [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) pode ser chamada a qualquer momento em qualquer thread.</span><span class="sxs-lookup"><span data-stu-id="bfe46-104">Although a [recognizer context](hrecocontext-handle.md) cannot be accessed on two threads simultaneously by the Tablet PC platform, the [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) function can be called at any time on any thread.</span></span> <span data-ttu-id="bfe46-105">Como a plataforma Tablet PC não garante que haja apenas um contexto de reconhecedor por vez, dois contextos de reconhecedor separados em threads separados podem tentar acessar simultaneamente o [reconhecedor](hrecognizer-handle.md).</span><span class="sxs-lookup"><span data-stu-id="bfe46-105">Because the Tablet PC platform does not ensure that there is only one recognizer context at a time, two separate recognizer contexts in separate threads may simultaneously attempt to access your [recognizer](hrecognizer-handle.md).</span></span> <span data-ttu-id="bfe46-106">Portanto, as variáveis globais em seu mecanismo de reconhecimento devem ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="bfe46-106">Therefore, global variables in your recognition engine must be thread-safe.</span></span>

<span data-ttu-id="bfe46-107">As listas de palavras são uma implementação opcional usada para aumentar a precisão.</span><span class="sxs-lookup"><span data-stu-id="bfe46-107">Word lists are an optional implementation used to increase accuracy.</span></span> <span data-ttu-id="bfe46-108">Se o reconhecedor implementar listas de palavras, ele deverá ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="bfe46-108">If your recognizer implements word lists, it must be thread-safe.</span></span> <span data-ttu-id="bfe46-109">Para obter mais informações sobre como usar listas de palavras, consulte [usando dicionários de aplicativos](using-application-dictionaries.md).</span><span class="sxs-lookup"><span data-stu-id="bfe46-109">For more information about using word lists, see [Using Application Dictionaries](using-application-dictionaries.md).</span></span>

<span data-ttu-id="bfe46-110">Para obter detalhes sobre outras considerações sobre Threading, consulte [considerações de Threading do Tablet PC](tablet-pc-threading-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="bfe46-110">For details about other threading considerations, see [Tablet PC Threading Considerations](tablet-pc-threading-considerations.md).</span></span>

 

 



