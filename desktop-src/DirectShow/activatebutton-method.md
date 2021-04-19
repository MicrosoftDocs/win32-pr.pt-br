---
description: O método ActivateButton ativa o botão de menu selecionado.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Método ActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a463a3aad1ee0dcabc0e5daaa4a4969efa37aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105767698"
---
# <a name="activatebutton-method"></a><span data-ttu-id="241cc-103">Método ActivateButton</span><span class="sxs-lookup"><span data-stu-id="241cc-103">ActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="241cc-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="241cc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="241cc-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="241cc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="241cc-106">O método ActivateButton ativa o botão de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="241cc-106">The ActivateButton method activates the selected menu button.</span></span>

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a><span data-ttu-id="241cc-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="241cc-107">Return Value</span></span>

<span data-ttu-id="241cc-108">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="241cc-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="241cc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="241cc-109">Remarks</span></span>

<span data-ttu-id="241cc-110">Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="241cc-110">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="241cc-111">Use este método para ativar um botão que foi selecionado por meio do método [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md)ou [**SelectRightButton**](selectrightbutton-method.md) .</span><span class="sxs-lookup"><span data-stu-id="241cc-111">Use this method to activate a button that has been selected through the [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), or [**SelectRightButton**](selectrightbutton-method.md) method.</span></span>

 

 



