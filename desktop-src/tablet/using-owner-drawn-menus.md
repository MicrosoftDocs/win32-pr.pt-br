---
description: Usando os menus desenhados pelo proprietário para dar suporte à funcionalidade de fala para o Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Usando Owner-Drawn menus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647092"
---
# <a name="using-owner-drawn-menus"></a><span data-ttu-id="c8671-103">Usando Owner-Drawn menus</span><span class="sxs-lookup"><span data-stu-id="c8671-103">Using Owner-Drawn Menus</span></span>

<span data-ttu-id="c8671-104">Ao usar menus desenhados pelo proprietário, você deve disponibilizar os nomes de menu para dar suporte à funcionalidade de fala.</span><span class="sxs-lookup"><span data-stu-id="c8671-104">When using owner-drawn menus, you must make the menu names available to support speech functionality.</span></span> <span data-ttu-id="c8671-105">Há duas maneiras de fazer isso:</span><span class="sxs-lookup"><span data-stu-id="c8671-105">There are two ways to do this:</span></span>

-   <span data-ttu-id="c8671-106">Expor o nome do item de menu usando a estrutura MSAAMENUINFO.</span><span class="sxs-lookup"><span data-stu-id="c8671-106">Expose the menu item name by using the MSAAMENUINFO structure.</span></span>
-   <span data-ttu-id="c8671-107">Forneça uma opção para substituir os menus gráficos por menus de texto padrão quando um auxílio de acessibilidade estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="c8671-107">Provide an option to replace graphic menus with standard text menus when an accessibility aid is active.</span></span> <span data-ttu-id="c8671-108">Se a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) retornar **true** com seu parâmetro *uiAction* definido como SPI \_ GETSCREENREADER, use os menus padrão. O aplicativo deve observar a \_ mensagem SETTINGSCHANGE do WM e responder consultando o estado dessa opção e ajustando sua exibição adequadamente.</span><span class="sxs-lookup"><span data-stu-id="c8671-108">If the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function returns **TRUE** with its *uiAction* parameter set to SPI\_GETSCREENREADER, use standard menus.The application should watch for the WM\_SETTINGSCHANGE message and respond by querying the state of this option and adjusting its display appropriately.</span></span> <span data-ttu-id="c8671-109">Por exemplo, Microsoft Visual Studio fornece uma opção para usar menus padrão em vez dos menus personalizados que são exibidos por padrão.</span><span class="sxs-lookup"><span data-stu-id="c8671-109">For example, Microsoft Visual Studio provides an option to use standard menus instead of the custom menus that are displayed by default.</span></span>

 

 
