---
title: UI_PKEY_FontProperties_Bold
description: Identifica a propriedade \_ FontProperties Bold da PKEY \_ da interface do \_ usuário.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444377"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="c7155-103">\_ \_ FontProperties PKEY da interface do usuário em \_ negrito</span><span class="sxs-lookup"><span data-stu-id="c7155-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="c7155-104">Identifica a propriedade \_ FontProperties Bold da PKEY \_ da interface do \_ usuário.</span><span class="sxs-lookup"><span data-stu-id="c7155-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="c7155-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7155-105">Remarks</span></span>

<span data-ttu-id="c7155-106">FontProperties Bold da interface do usuário PKEY é usada por um aplicativo \_ para consultar o estado do botão \_ \_ **Negrito.**</span><span class="sxs-lookup"><span data-stu-id="c7155-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="c7155-107">O valor da propriedade é da [**enumeração \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7155-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="c7155-108">O valor padrão é `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="c7155-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="c7155-109">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c7155-109">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="c7155-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c7155-110">Property</span></span>                    |    <span data-ttu-id="c7155-111">Resultado da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c7155-111">UI Result</span></span>                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="c7155-112">**O** botão negrito está desabilitado e só pode ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7155-112">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="c7155-113">**O** botão Negrito não está selecionado.</span><span class="sxs-lookup"><span data-stu-id="c7155-113">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="c7155-114">**O botão** Negrito está selecionado.</span><span class="sxs-lookup"><span data-stu-id="c7155-114">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="c7155-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7155-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7155-116">Propriedades do controle de fonte</span><span class="sxs-lookup"><span data-stu-id="c7155-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="c7155-117">**\_FONTPROPERTIES da interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="c7155-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="c7155-118">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="c7155-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 