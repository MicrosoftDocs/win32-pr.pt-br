---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444297"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="22719-103">Interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="22719-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="22719-104">Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning.</span><span class="sxs-lookup"><span data-stu-id="22719-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="22719-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="22719-105">Remarks</span></span>

<span data-ttu-id="22719-106">A interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning é usada por um aplicativo para consultar o valor dos controles **sobrescrito** e **subscrito** .</span><span class="sxs-lookup"><span data-stu-id="22719-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="22719-107">O valor da propriedade é da [**enumeração \_ FONTVERTICALPOSITION da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) .</span><span class="sxs-lookup"><span data-stu-id="22719-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="22719-108">O valor padrão é `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="22719-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="22719-109">A captura de tela a seguir mostra os botões **sobrescrito** e **subscrito** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="22719-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="22719-111">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="22719-111">The following table describes the properties and the UI result.</span></span>



|     <span data-ttu-id="22719-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="22719-112">Property</span></span>                           |          <span data-ttu-id="22719-113">Resultado da IU</span><span class="sxs-lookup"><span data-stu-id="22719-113">UI Result</span></span>                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="22719-114">Os botões **sobrescrito** e **subscrito** estão desabilitados e só podem ser definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22719-114">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="22719-115">Os botões **sobrescrito** e **subscrito** não estão selecionados.</span><span class="sxs-lookup"><span data-stu-id="22719-115">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="22719-116">O botão **sobrescrito** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="22719-116">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="22719-117">O botão **subscrito** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="22719-117">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="22719-118">Os botões **sobrescrito** e **subscrito** não podem ser selecionados.</span><span class="sxs-lookup"><span data-stu-id="22719-118">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="22719-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22719-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22719-120">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="22719-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="22719-121">**FONTVERTICALPOSITION da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="22719-121">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="22719-122">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="22719-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 