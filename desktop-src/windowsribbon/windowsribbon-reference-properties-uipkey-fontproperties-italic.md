---
title: UI_PKEY_FontProperties_Italic
description: Identifica a propriedade \_ IU PKEY \_ FontProperties \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443807"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="c5be9-103">Fonte \_ de PKEY \_ da interface do usuárioPropriedades \_ itálico</span><span class="sxs-lookup"><span data-stu-id="c5be9-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="c5be9-104">Identifica a propriedade \_ IU PKEY \_ FontProperties \_ Italic.</span><span class="sxs-lookup"><span data-stu-id="c5be9-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="c5be9-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5be9-105">Remarks</span></span>

<span data-ttu-id="c5be9-106">A \_ interface do usuário \_ PKEY FontProperties Italic é usada por um aplicativo para consultar o \_ estado do botão **Itálico.**</span><span class="sxs-lookup"><span data-stu-id="c5be9-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="c5be9-107">O valor da propriedade é da [**enumeração \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c5be9-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="c5be9-108">O valor padrão é `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="c5be9-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="c5be9-109">A tabela a seguir descreve as propriedades e o resultado da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c5be9-109">The following table describes the properties and the UI result.</span></span>



|    <span data-ttu-id="c5be9-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c5be9-110">Property</span></span>                      |       <span data-ttu-id="c5be9-111">Resultado da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c5be9-111">UI Result</span></span>                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="c5be9-112">**O botão Itálico** está desabilitado e só pode ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5be9-112">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="c5be9-113">**O botão Itálico** não está selecionado.</span><span class="sxs-lookup"><span data-stu-id="c5be9-113">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="c5be9-114">**O botão Itálico** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="c5be9-114">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="c5be9-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5be9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5be9-116">Propriedades do controle de fonte</span><span class="sxs-lookup"><span data-stu-id="c5be9-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="c5be9-117">**\_FONTPROPERTIES da interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="c5be9-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="c5be9-118">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="c5be9-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 