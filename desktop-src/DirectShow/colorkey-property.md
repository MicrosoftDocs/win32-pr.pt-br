---
description: A propriedade ColorKey define ou recupera a chave de cor usada em legendas ocultas.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Propriedade ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456489"
---
# <a name="colorkey-property"></a><span data-ttu-id="c1bf0-103">Propriedade ColorKey</span><span class="sxs-lookup"><span data-stu-id="c1bf0-103">ColorKey Property</span></span>

> [!Note]  
> <span data-ttu-id="c1bf0-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c1bf0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c1bf0-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c1bf0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c1bf0-106">A `ColorKey` propriedade define ou recupera a chave de cor usada em Legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="c1bf0-106">The `ColorKey` property sets or retrieves the color key used in closed captioning.</span></span>

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a><span data-ttu-id="c1bf0-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c1bf0-107">Return Value</span></span>

<span data-ttu-id="c1bf0-108">Retorna um valor inteiro que representa a cor a ser usada como um plano de fundo transparente para texto com legenda codificada.</span><span class="sxs-lookup"><span data-stu-id="c1bf0-108">Returns an integer value representing the color to use as a transparent background for closed-captioned text.</span></span> <span data-ttu-id="c1bf0-109">O valor padrão em 256 cores é magenta e off-preto em qualquer outra intensidade de cor.</span><span class="sxs-lookup"><span data-stu-id="c1bf0-109">The default value in 256 colors is magenta, and off-black in any other color depth.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1bf0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1bf0-110">Remarks</span></span>

<span data-ttu-id="c1bf0-111">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c1bf0-111">This property is read/write.</span></span> <span data-ttu-id="c1bf0-112">Essa propriedade só se aplica a legendas fechadas, se existir, não ao fluxo de subimagem.</span><span class="sxs-lookup"><span data-stu-id="c1bf0-112">This property applies only to the closed-captions, if any exist, not to the subpicture stream.</span></span>

 

 



