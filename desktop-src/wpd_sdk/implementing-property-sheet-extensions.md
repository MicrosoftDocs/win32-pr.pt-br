---
description: Implementando extensões de folha de propriedades
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implementando extensões de folha de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768350"
---
# <a name="implementing-property-sheet-extensions"></a><span data-ttu-id="92d67-103">Implementando extensões de folha de propriedades</span><span class="sxs-lookup"><span data-stu-id="92d67-103">Implementing Property Sheet Extensions</span></span>

<span data-ttu-id="92d67-104">A extensão do namespace WPD dá suporte a folhas de propriedades extensíveis.</span><span class="sxs-lookup"><span data-stu-id="92d67-104">The WPD Namespace Extension supports extensible property sheets.</span></span> <span data-ttu-id="92d67-105">Essas são as caixas de diálogo de propriedade que aparecem quando um usuário clica com o botão direito do mouse em um objeto, como um arquivo ou uma pasta, e seleciona **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="92d67-105">These are the property dialogs that appear when a user right-clicks on an object, such as a file or a folder, and selects **Properties**.</span></span> <span data-ttu-id="92d67-106">Alguns aplicativos WPD aproveitam essas folhas de propriedades extensível para exibir propriedades de conteúdo do lado do dispositivo (ou objetos que residem no dispositivo).</span><span class="sxs-lookup"><span data-stu-id="92d67-106">Some WPD applications will take advantage of these extensible property sheets to display properties for device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="92d67-107">As interfaces de propriedades extensíveis são suportadas pela interface descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="92d67-107">Extensible property sheets are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="92d67-108">Para obter mais informações sobre qualquer uma dessas interfaces, consulte a SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="92d67-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="92d67-109">Interface</span><span class="sxs-lookup"><span data-stu-id="92d67-109">Interface</span></span>           | <span data-ttu-id="92d67-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="92d67-110">Description</span></span>                                                                  |
|---------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="92d67-111">IDataObject</span><span class="sxs-lookup"><span data-stu-id="92d67-111">IDataObject</span></span>         | <span data-ttu-id="92d67-112">Usado para passar a matriz PIDL do menu de contexto para o manipulador de menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="92d67-112">Used to pass the context menu's PIDL array to the context menu handler.</span></span>      |
| <span data-ttu-id="92d67-113">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="92d67-113">IPropertySetStorage</span></span> | <span data-ttu-id="92d67-114">Essa interface é usada para recuperar as propriedades de WPD para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="92d67-114">This interface is used to retrieve WPD properties for the given object.</span></span>      |
| <span data-ttu-id="92d67-115">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="92d67-115">IPropertyStorage</span></span>    | <span data-ttu-id="92d67-116">Essa interface também é usada para recuperar as propriedades de WPD para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="92d67-116">This interface is also used to retrieve WPD properties for the given object.</span></span> |
| <span data-ttu-id="92d67-117">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="92d67-117">IShellExtInit</span></span>       | <span data-ttu-id="92d67-118">Inicializa as extensões do shell do Windows Vista para o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="92d67-118">Initializes the Windows Vista Shell extensions for the context menu.</span></span>         |
| <span data-ttu-id="92d67-119">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="92d67-119">IShellPropSheetExt</span></span>  | <span data-ttu-id="92d67-120">Dá suporte à adição de extensões de folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="92d67-120">Supports addition of property sheet extensions.</span></span>                              |



 

<span data-ttu-id="92d67-121">Folhas de propriedades para WPD são implementadas como qualquer outra folha de propriedades no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92d67-121">Property sheets for WPD are implemented like any other property sheet in Windows Vista.</span></span> <span data-ttu-id="92d67-122">Se você já tiver implementado um manipulador de folha de propriedades, poderá modificar o código existente para que ele dê suporte ao conteúdo do lado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92d67-122">If you've already implemented a property sheet handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="92d67-123">Se você nunca criou um manipulador de menu de contexto, consulte o tópico Criando manipuladores de folha de propriedades na SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="92d67-123">If you've never created a context menu handler, see the Creating Property Sheet Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="92d67-124">Os dois pontos em que um manipulador de folha de propriedades WPD difere de qualquer outro manipulador está no registro do manipulador e no suporte ao conteúdo do lado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92d67-124">The two points at which a WPD property sheet handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



