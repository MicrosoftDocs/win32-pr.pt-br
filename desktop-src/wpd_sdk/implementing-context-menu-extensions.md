---
description: Implementando extensões do menu de contexto
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: Implementando extensões do menu de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812346"
---
# <a name="implementing-context-menu-extensions"></a><span data-ttu-id="518da-103">Implementando extensões do menu de contexto</span><span class="sxs-lookup"><span data-stu-id="518da-103">Implementing Context Menu Extensions</span></span>

<span data-ttu-id="518da-104">A extensão de namespace WPD dá suporte a menus de contexto extensível (ou atalho).</span><span class="sxs-lookup"><span data-stu-id="518da-104">The WPD Namespace Extension supports extensible context (or shortcut) menus.</span></span> <span data-ttu-id="518da-105">Esses são os menus que aparecem quando um usuário clica com o botão direito do mouse em um objeto, como um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="518da-105">These are the menus that appear when a user right-clicks on an object such as a file or a folder.</span></span> <span data-ttu-id="518da-106">Alguns aplicativos WPD aproveitam esses menus extensíveis para dar suporte a operações no conteúdo do lado do dispositivo (ou objetos que residem no dispositivo).</span><span class="sxs-lookup"><span data-stu-id="518da-106">Some WPD applications will take advantage of these extensible menus to support operations on device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="518da-107">Os menus de contexto extensível têm suporte nas interfaces descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="518da-107">Extensible context menus are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="518da-108">Para obter mais informações sobre qualquer uma dessas interfaces, consulte a SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="518da-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="518da-109">Interface</span><span class="sxs-lookup"><span data-stu-id="518da-109">Interface</span></span>           | <span data-ttu-id="518da-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="518da-110">Description</span></span>                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="518da-111">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="518da-111">IContextMenu</span></span>        | <span data-ttu-id="518da-112">O Shell do Windows Vista chama os métodos nesta interface para criar ou mesclar o novo menu de contexto com o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="518da-112">The Windows Vista Shell calls the methods in this interface to create or merge the new context menu with the given object.</span></span> |
| <span data-ttu-id="518da-113">IDataObject</span><span class="sxs-lookup"><span data-stu-id="518da-113">IDataObject</span></span>         | <span data-ttu-id="518da-114">Usado para passar a matriz PIDL do menu de contexto para o manipulador de menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="518da-114">Used to pass the context menu's PIDL array to the context menu handler.</span></span>                                                    |
| <span data-ttu-id="518da-115">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="518da-115">IPropertySetStorage</span></span> | <span data-ttu-id="518da-116">Essa interface é usada para recuperar as propriedades de WPD para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="518da-116">This interface is used to retrieve WPD properties for the given object.</span></span>                                                    |
| <span data-ttu-id="518da-117">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="518da-117">IPropertyStorage</span></span>    | <span data-ttu-id="518da-118">Essa interface também é usada para recuperar as propriedades de WPD para o objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="518da-118">This interface is also used to retrieve WPD properties for the given object.</span></span>                                               |
| <span data-ttu-id="518da-119">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="518da-119">IShellExtInit</span></span>       | <span data-ttu-id="518da-120">Inicializa as extensões do shell do Windows Vista para o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="518da-120">Initializes the Windows Vista Shell extensions for the context menu.</span></span>                                                       |
| <span data-ttu-id="518da-121">IStream</span><span class="sxs-lookup"><span data-stu-id="518da-121">IStream</span></span>             | <span data-ttu-id="518da-122">A ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="518da-122">To be supplied.</span></span>                                                                                                            |



 

<span data-ttu-id="518da-123">Os menus de contexto para WPD são implementados como qualquer outro menu de contexto no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="518da-123">Context menus for WPD are implemented like any other context menu in Windows Vista.</span></span> <span data-ttu-id="518da-124">Se você já tiver implementado um manipulador de menu de contexto, poderá modificar o código existente para que ele dê suporte ao conteúdo do lado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="518da-124">If you've already implemented a context menu handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="518da-125">Se você nunca criou um manipulador de menu de contexto, consulte o tópico Criando manipuladores de menu de contexto na SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="518da-125">If you have never created a context menu handler, see the Creating Context Menu Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="518da-126">Os dois pontos em que um manipulador de menu de contexto WPD difere de qualquer outro manipulador está no registro do manipulador e no suporte ao conteúdo do lado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="518da-126">The two points at which a WPD context menu handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



