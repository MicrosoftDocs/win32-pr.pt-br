---
title: UI_PKEY_FontProperties_Italic
description: Identifica a propriedade de itálico da interface do usuário \_ PKEY \_ fontproperties \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366155"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="838c8-103">Interface do usuário \_ PKEY \_ fontproperties \_ itálico</span><span class="sxs-lookup"><span data-stu-id="838c8-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="838c8-104">Identifica a propriedade de itálico da interface do usuário \_ PKEY \_ fontproperties \_ .</span><span class="sxs-lookup"><span data-stu-id="838c8-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="838c8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="838c8-105">Remarks</span></span>

<span data-ttu-id="838c8-106">A interface do usuário \_ PKEY \_ FontProperty \_ Italic é usada por um aplicativo para consultar o estado do botão **itálico** .</span><span class="sxs-lookup"><span data-stu-id="838c8-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="838c8-107">O valor da propriedade é da [**enumeração \_ fontproperties da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="838c8-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="838c8-108">O valor padrão é `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="838c8-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="838c8-109">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="838c8-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="838c8-110">O botão **itálico** está desabilitado e só pode ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="838c8-110">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="838c8-111">O botão **itálico** não está selecionado.</span><span class="sxs-lookup"><span data-stu-id="838c8-111">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="838c8-112">O botão **itálico** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="838c8-112">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="838c8-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="838c8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="838c8-114">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="838c8-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="838c8-115">**fonte de fontes da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="838c8-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="838c8-116">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="838c8-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 