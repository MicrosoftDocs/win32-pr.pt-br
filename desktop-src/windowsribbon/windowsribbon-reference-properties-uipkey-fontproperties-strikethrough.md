---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica a \_ propriedade de \_ tachado PKEY fontproperties de interface do usuário \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b684704fdd90a8dd1b88b14db2b52540b15fccb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443787"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="970e1-103">Interface do usuário \_ PKEY \_ fontproperties \_ tachado</span><span class="sxs-lookup"><span data-stu-id="970e1-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="970e1-104">Identifica a \_ propriedade de \_ tachado PKEY fontproperties de interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="970e1-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="970e1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="970e1-105">Remarks</span></span>

<span data-ttu-id="970e1-106">A interface do usuário \_ PKEY \_ fontproperties \_ tachado é usada por um aplicativo para consultar o estado do botão **tachado** .</span><span class="sxs-lookup"><span data-stu-id="970e1-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="970e1-107">O valor da propriedade é da [**enumeração \_ fontproperties da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="970e1-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="970e1-108">O valor padrão é `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="970e1-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="970e1-109">A captura de tela a seguir mostra o botão **tachado** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="970e1-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="970e1-111">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="970e1-111">The following table describes the properties and the UI result.</span></span>



|   <span data-ttu-id="970e1-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="970e1-112">Property</span></span>                       |    <span data-ttu-id="970e1-113">Resultado da IU</span><span class="sxs-lookup"><span data-stu-id="970e1-113">UI Result</span></span>                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="970e1-114">O botão **tachado** está desabilitado e só pode ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="970e1-114">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="970e1-115">O botão **tachado** não está selecionado.</span><span class="sxs-lookup"><span data-stu-id="970e1-115">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="970e1-116">O botão **tachado** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="970e1-116">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="970e1-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="970e1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="970e1-118">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="970e1-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="970e1-119">**fonte de fontes da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="970e1-119">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="970e1-120">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="970e1-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 