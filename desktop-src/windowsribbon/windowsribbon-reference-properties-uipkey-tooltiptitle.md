---
title: UI_PKEY_TooltipTitle
description: Identifica a \_ Propriedade PKEY TooltipTitle da interface do usuário \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798379"
---
# <a name="ui_pkey_tooltiptitle"></a><span data-ttu-id="4056f-103">\_TooltipTitle PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="4056f-103">UI\_PKEY\_TooltipTitle</span></span>

<span data-ttu-id="4056f-104">Identifica a \_ Propriedade PKEY TooltipTitle da interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="4056f-104">Identifies the UI\_PKEY\_TooltipTitle property.</span></span>

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="4056f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="4056f-105">Remarks</span></span>

<span data-ttu-id="4056f-106">A interface do usuário \_ PKEY \_ TooltipTitle é usada por um aplicativo para consultar a dica de ferramenta de guias, grupos, botões, itens da galeria e outros controles da faixa de tipos.</span><span class="sxs-lookup"><span data-stu-id="4056f-106">UI\_PKEY\_TooltipTitle is used by an application to query the tooltip of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

<span data-ttu-id="4056f-107">O valor da propriedade é uma cadeia de caracteres restrita a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="4056f-107">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="4056f-108">Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="4056f-108">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="4056f-109">Não há suporte para alinhamento à direita.</span><span class="sxs-lookup"><span data-stu-id="4056f-109">Right alignment is not supported.</span></span>

<span data-ttu-id="4056f-110">O comprimento máximo da interface do usuário \_ PKEY \_ TooltipTitle é não associado.</span><span class="sxs-lookup"><span data-stu-id="4056f-110">The maximum length of UI\_PKEY\_TooltipTitle is unbounded.</span></span>

<span data-ttu-id="4056f-111">Para exibir um e comercial em uma dica de ferramenta, escape a designação de caractere especial com um e comercial duplo ( `&&` ), conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="4056f-111">To display an ampersand in a tooltip, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a><span data-ttu-id="4056f-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4056f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4056f-113">Propriedades do recurso</span><span class="sxs-lookup"><span data-stu-id="4056f-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="4056f-114">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="4056f-114">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[<span data-ttu-id="4056f-115">\_TooltipDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="4056f-115">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




