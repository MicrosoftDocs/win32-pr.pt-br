---
description: A propriedade subpictureize define ou recupera o estado atual da subimagem (ativado ou desativado).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Propriedade subpictureize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787130"
---
# <a name="subpictureon-property"></a><span data-ttu-id="c0ddf-103">Propriedade subpictureize</span><span class="sxs-lookup"><span data-stu-id="c0ddf-103">SubpictureOn Property</span></span>

> [!Note]  
> <span data-ttu-id="c0ddf-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c0ddf-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c0ddf-106">A `SubpictureOn` propriedade define ou recupera o estado da subimagem atual (ativado ou desativado).</span><span class="sxs-lookup"><span data-stu-id="c0ddf-106">The `SubpictureOn` property sets or retrieves the current subpicture state (on or off).</span></span>

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a><span data-ttu-id="c0ddf-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c0ddf-107">Return Value</span></span>

<span data-ttu-id="c0ddf-108">Retorna um valor booliano que indica se a subimagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-108">Returns a Boolean value indicating whether the subpicture is displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0ddf-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0ddf-109">Remarks</span></span>

<span data-ttu-id="c0ddf-110">Essa propriedade não afeta a exibição de legendas ocultas.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-110">This property does not affect display of Closed Captions.</span></span> <span data-ttu-id="c0ddf-111">As legendas ocultas são inseridas no fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-111">Closed Captions are embedded within the video stream.</span></span> <span data-ttu-id="c0ddf-112">As subimagems de DVD são transportadas em um fluxo separado.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-112">DVD subpictures are transported on a separate stream.</span></span>

<span data-ttu-id="c0ddf-113">Quando o fluxo de subimagem é alterado usando [**CurrentSubpictureStream**](currentsubpicturestream-property.md), a `SubpictureOn` Propriedade alterna para **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-113">When the subpicture stream is changed using [**CurrentSubpictureStream**](currentsubpicturestream-property.md), the `SubpictureOn` property toggles to **True**.</span></span>

<span data-ttu-id="c0ddf-114">Essa propriedade é de leitura/gravação com um valor padrão de false.</span><span class="sxs-lookup"><span data-stu-id="c0ddf-114">This property is read/write with a default value of false.</span></span>

 

 



