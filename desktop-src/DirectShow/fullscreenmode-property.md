---
description: A propriedade FullScreenmode define ou recupera um valor que indica se a exibição está no modo de tela inteira.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propriedade FullScreenmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087284"
---
# <a name="fullscreenmode-property"></a><span data-ttu-id="1ba54-103">Propriedade FullScreenmode</span><span class="sxs-lookup"><span data-stu-id="1ba54-103">FullScreenMode Property</span></span>

> [!Note]  
> <span data-ttu-id="1ba54-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1ba54-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1ba54-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1ba54-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1ba54-106">A `FullScreenMode` propriedade define ou recupera um valor que indica se a exibição está no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="1ba54-106">The `FullScreenMode` property sets or retrieves a value indicating whether the display is in full-screen mode.</span></span>

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a><span data-ttu-id="1ba54-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1ba54-107">Return Value</span></span>

<span data-ttu-id="1ba54-108">Retorna um valor booliano que indica se a reprodução de tela inteira deve ser habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1ba54-108">Returns a Boolean value indicating whether to enable or disable full-screen playback.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba54-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba54-109">Remarks</span></span>

<span data-ttu-id="1ba54-110">Essa propriedade é de leitura/gravação com um valor padrão de false.</span><span class="sxs-lookup"><span data-stu-id="1ba54-110">This property is read/write with a default value of false.</span></span>



| <span data-ttu-id="1ba54-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1ba54-111">Value</span></span> | <span data-ttu-id="1ba54-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ba54-112">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="1ba54-113">true</span><span class="sxs-lookup"><span data-stu-id="1ba54-113">true</span></span>  | <span data-ttu-id="1ba54-114">Habilite a reprodução em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="1ba54-114">Enable full-screen playback.</span></span> <span data-ttu-id="1ba54-115">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="1ba54-115">This is the default value</span></span> |
| <span data-ttu-id="1ba54-116">false</span><span class="sxs-lookup"><span data-stu-id="1ba54-116">false</span></span> | <span data-ttu-id="1ba54-117">Desabilite a reprodução em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="1ba54-117">Disable full-screen playback.</span></span>                          |



 

<span data-ttu-id="1ba54-118">O modo de tela inteira só está disponível quando o controle MSWebDVD está em execução no modo de janela.</span><span class="sxs-lookup"><span data-stu-id="1ba54-118">Full screen mode is only available when the MSWebDVD control is running in windowed mode.</span></span>

 

 



