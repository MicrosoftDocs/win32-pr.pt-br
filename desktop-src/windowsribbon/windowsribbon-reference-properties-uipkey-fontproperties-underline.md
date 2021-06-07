---
title: UI_PKEY_FontProperties_Underline
description: Identifica a propriedade sublinhada \_ \_ FontProperties PKEY da interface do \_ usuário.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443777"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="01a10-103">\_Sublinhado FontProperties de PKEY \_ \_ da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="01a10-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="01a10-104">Identifica a propriedade sublinhada \_ \_ FontProperties PKEY da interface do \_ usuário.</span><span class="sxs-lookup"><span data-stu-id="01a10-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="01a10-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="01a10-105">Remarks</span></span>

<span data-ttu-id="01a10-106">O sublinhado FontProperties PKEY da interface do usuário é usado por um aplicativo para consultar o \_ \_ estado do botão \_ **Sublinhado.**</span><span class="sxs-lookup"><span data-stu-id="01a10-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="01a10-107">O valor da propriedade é da [**enumeração \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="01a10-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="01a10-108">O valor padrão é `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="01a10-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="01a10-109">A captura de tela a seguir mostra **o botão Sublinhado** do FontControl da Faixa [**de Opções.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="01a10-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="01a10-111">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="01a10-111">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="01a10-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="01a10-112">Property</span></span>                   |       <span data-ttu-id="01a10-113">Resultado da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="01a10-113">UI Result</span></span>                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="01a10-114">**O botão** sublinhado está desabilitado e só pode ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01a10-114">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="01a10-115">**O botão** Sublinhado não está selecionado.</span><span class="sxs-lookup"><span data-stu-id="01a10-115">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="01a10-116">**O botão** Sublinhado está selecionado.</span><span class="sxs-lookup"><span data-stu-id="01a10-116">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="01a10-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01a10-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a10-118">Propriedades do controle de fonte</span><span class="sxs-lookup"><span data-stu-id="01a10-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="01a10-119">**\_FONTUNDERLINE DA INTERFACE DO USUÁRIO**</span><span class="sxs-lookup"><span data-stu-id="01a10-119">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="01a10-120">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="01a10-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 