---
description: A propriedade DisableAutoMouseProcessing habilita ou desabilita a funcionalidade de processamento de mouse do objeto MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Propriedade DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456409"
---
# <a name="disableautomouseprocessing-property"></a><span data-ttu-id="991ac-103">Propriedade DisableAutoMouseProcessing</span><span class="sxs-lookup"><span data-stu-id="991ac-103">DisableAutoMouseProcessing Property</span></span>

> [!Note]  
> <span data-ttu-id="991ac-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="991ac-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="991ac-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="991ac-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="991ac-106">A `DisableAutoMouseProcessing` Propriedade habilita ou desabilita a funcionalidade de processamento de mouse do objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="991ac-106">The `DisableAutoMouseProcessing` property enables or disables the **MSWebDVD** object's mouse-processing functionality.</span></span>

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a><span data-ttu-id="991ac-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="991ac-107">Return Value</span></span>

<span data-ttu-id="991ac-108">Retorna um valor booliano que indica se o processamento padrão do mouse deve ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="991ac-108">Returns a boolean value indicating whether to disable the default mouse processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="991ac-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="991ac-109">Remarks</span></span>

<span data-ttu-id="991ac-110">Essa propriedade é de leitura/gravação com um valor padrão de false.</span><span class="sxs-lookup"><span data-stu-id="991ac-110">This property is read/write with a default value of false.</span></span> <span data-ttu-id="991ac-111">O objeto **MSWebDVD** manipula automaticamente ações do mouse para menus na tela de DVD por padrão; os usuários podem realçar e ativar botões de menu sem programação especial pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="991ac-111">The **MSWebDVD** object automatically handles mouse actions for DVD on-screen menus by default; users can highlight and activate menu buttons without special programming by the application.</span></span> <span data-ttu-id="991ac-112">Um aplicativo pode desativar essa funcionalidade padrão de manipulação de mouse definindo essa propriedade como **true**.</span><span class="sxs-lookup"><span data-stu-id="991ac-112">An application can turn off this default mouse-handling functionality by setting this property to **true**.</span></span> <span data-ttu-id="991ac-113">Quando o processamento automático do mouse é desativado, um aplicativo deve usar os vários métodos e propriedades relacionados ao botão para manipular as movimentações do mouse e os cliques do mouse nos menus na tela.</span><span class="sxs-lookup"><span data-stu-id="991ac-113">When the automatic mouse processing is turned off, an application must use the various button-related methods and properties to handle mouse moves and mouse clicks on the on-screen menus.</span></span> <span data-ttu-id="991ac-114">Além disso, um aplicativo pode usar os métodos relacionados ao botão para substituir a manipulação automática do mouse, mesmo quando `DisableAutoMouseProcessing` é definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="991ac-114">Also, an application can use the button-related methods to override the automatic mouse handling even when when `DisableAutoMouseProcessing` is set to **false**.</span></span>

 

 



