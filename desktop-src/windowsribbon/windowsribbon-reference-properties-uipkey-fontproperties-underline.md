---
title: UI_PKEY_FontProperties_Underline
description: Identifica a \_ propriedade de \_ sublinhado PKEY fontproperties subinterface \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454182"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="402e7-103">Interface do usuário \_ PKEY \_ fontproperties \_ sublinhado</span><span class="sxs-lookup"><span data-stu-id="402e7-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="402e7-104">Identifica a \_ propriedade de \_ sublinhado PKEY fontproperties subinterface \_ .</span><span class="sxs-lookup"><span data-stu-id="402e7-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="402e7-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="402e7-105">Remarks</span></span>

<span data-ttu-id="402e7-106">A interface do usuário \_ PKEY \_ FontProperty \_ Underline é usada por um aplicativo para consultar o estado do botão **sublinhado** .</span><span class="sxs-lookup"><span data-stu-id="402e7-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="402e7-107">O valor da propriedade é da [**enumeração \_ FonteSublinhada da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .</span><span class="sxs-lookup"><span data-stu-id="402e7-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="402e7-108">O valor padrão é `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="402e7-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="402e7-109">A captura de tela a seguir mostra o botão **sublinhado** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="402e7-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="402e7-111">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="402e7-111">The following table describes the properties and the UI result.</span></span>



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="402e7-112">O botão **sublinhado** está desabilitado e só pode ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="402e7-112">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="402e7-113">O botão **sublinhado** não está selecionado.</span><span class="sxs-lookup"><span data-stu-id="402e7-113">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="402e7-114">O botão **sublinhado** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="402e7-114">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="402e7-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="402e7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="402e7-116">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="402e7-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="402e7-117">**FonteSublinhada da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="402e7-117">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="402e7-118">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="402e7-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 