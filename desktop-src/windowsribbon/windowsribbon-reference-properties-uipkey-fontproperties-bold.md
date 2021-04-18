---
title: UI_PKEY_FontProperties_Bold
description: Identifica a propriedade de interface de usuário \_ PKEY \_ FontProperty \_ Bold.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813597"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="bbed3-103">Interface do usuário \_ PKEY \_ FontProperty \_ bold</span><span class="sxs-lookup"><span data-stu-id="bbed3-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="bbed3-104">Identifica a propriedade de interface de usuário \_ PKEY \_ FontProperty \_ Bold.</span><span class="sxs-lookup"><span data-stu-id="bbed3-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="bbed3-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbed3-105">Remarks</span></span>

<span data-ttu-id="bbed3-106">A interface do usuário \_ PKEY \_ FontProperty \_ Bold é usada por um aplicativo para consultar o estado do botão **negrito** .</span><span class="sxs-lookup"><span data-stu-id="bbed3-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="bbed3-107">O valor da propriedade é da [**enumeração \_ fontproperties da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="bbed3-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="bbed3-108">O valor padrão é `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="bbed3-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="bbed3-109">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="bbed3-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="bbed3-110">O botão **negrito** está desabilitado e só pode ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bbed3-110">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="bbed3-111">O botão **negrito** não está selecionado.</span><span class="sxs-lookup"><span data-stu-id="bbed3-111">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="bbed3-112">O botão **negrito** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="bbed3-112">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="bbed3-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbed3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbed3-114">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="bbed3-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="bbed3-115">**fonte de fontes da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="bbed3-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="bbed3-116">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="bbed3-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 