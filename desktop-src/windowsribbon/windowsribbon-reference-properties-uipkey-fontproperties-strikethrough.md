---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica a \_ propriedade de \_ tachado PKEY fontproperties de interface do usuário \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366550"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="781e2-103">Interface do usuário \_ PKEY \_ fontproperties \_ tachado</span><span class="sxs-lookup"><span data-stu-id="781e2-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="781e2-104">Identifica a \_ propriedade de \_ tachado PKEY fontproperties de interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="781e2-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="781e2-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="781e2-105">Remarks</span></span>

<span data-ttu-id="781e2-106">A interface do usuário \_ PKEY \_ fontproperties \_ tachado é usada por um aplicativo para consultar o estado do botão **tachado** .</span><span class="sxs-lookup"><span data-stu-id="781e2-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="781e2-107">O valor da propriedade é da [**enumeração \_ fontproperties da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="781e2-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="781e2-108">O valor padrão é `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="781e2-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="781e2-109">A captura de tela a seguir mostra o botão **tachado** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="781e2-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="781e2-111">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="781e2-111">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="781e2-112">O botão **tachado** está desabilitado e só pode ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="781e2-112">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="781e2-113">O botão **tachado** não está selecionado.</span><span class="sxs-lookup"><span data-stu-id="781e2-113">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="781e2-114">O botão **tachado** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="781e2-114">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="781e2-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="781e2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="781e2-116">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="781e2-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="781e2-117">**fonte de fontes da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="781e2-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="781e2-118">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="781e2-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 