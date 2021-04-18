---
description: Descrição da identificação de uma janela por sua função para o Tablet PC.
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: Identificando uma janela por sua função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497f660d6690bd4dc37c252f82f2408da3e3655d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807986"
---
# <a name="identifying-a-window-by-its-function"></a><span data-ttu-id="effc5-103">Identificando uma janela por sua função</span><span class="sxs-lookup"><span data-stu-id="effc5-103">Identifying a Window by Its Function</span></span>

<span data-ttu-id="effc5-104">Identifique cada tipo de janela atribuindo a ela uma classe de janela exclusiva.</span><span class="sxs-lookup"><span data-stu-id="effc5-104">Identify each type of window by assigning it a unique window class.</span></span> <span data-ttu-id="effc5-105">Evite ter uma única classe de janela que seja usada para uma ampla variedade de funções.</span><span class="sxs-lookup"><span data-stu-id="effc5-105">Avoid having a single window class that is used for a wide variety of functions.</span></span>

<span data-ttu-id="effc5-106">Os auxílios de acessibilidade devem ter essa identificação para lidar com janelas diferentes no mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="effc5-106">Accessibility aids must have this identification in order to handle different windows within the same application.</span></span> <span data-ttu-id="effc5-107">Pode haver instruções separadas para lidar com essas janelas, como anunciar áreas específicas quando o conteúdo é alterado.</span><span class="sxs-lookup"><span data-stu-id="effc5-107">There may be separate instructions for handling these windows, such as announcing specific areas when the content changes.</span></span>

<span data-ttu-id="effc5-108">Se você não puder usar classes de janela separadas, poderá expor as diferenças por meio do Microsoft <entity type="reg"/> acessibilidade ativa <entity type="reg"/> ou, se necessário, por uma mensagem de janela particular que você documenta em seu site.</span><span class="sxs-lookup"><span data-stu-id="effc5-108">If you cannot use separate window classes, you can expose the differences through Microsoft<entity type="reg"/> Active Accessibility<entity type="reg"/>, or if necessary, by a private window message that you document on your website.</span></span>

<span data-ttu-id="effc5-109">Para obter mais informações sobre como expor classes de janela usando Acessibilidade Ativa, consulte a seção [acessibilidade](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="effc5-109">For more information about exposing window classes by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
