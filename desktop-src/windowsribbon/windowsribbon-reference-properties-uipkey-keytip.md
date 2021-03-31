---
title: UI_PKEY_Keytip
description: Identifica a \_ Propriedade PKEY KeyTip da interface do usuário \_ .
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916339"
---
# <a name="ui_pkey_keytip"></a><span data-ttu-id="c522b-103">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c522b-103">UI\_PKEY\_Keytip</span></span>

<span data-ttu-id="c522b-104">Identifica a \_ Propriedade PKEY KeyTip da interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="c522b-104">Identifies the UI\_PKEY\_Keytip property.</span></span>

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="c522b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c522b-105">Remarks</span></span>

<span data-ttu-id="c522b-106">A interface do usuário \_ PKEY \_ KeyTip é usada por um aplicativo para consultar o acelerador de teclado de um controle da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="c522b-106">UI\_PKEY\_Keytip is used by an application to query the keyboard accelerator of a ribbon control.</span></span>

<span data-ttu-id="c522b-107">Esse valor de propriedade é uma cadeia de caracteres, composta de qualquer sequência de caracteres, incluindo o espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="c522b-107">This property value is a string, composed of any sequence of characters including white space.</span></span>

<span data-ttu-id="c522b-108">O valor da interface do usuário \_ PKEY \_ KeyTip atua como o acelerador de teclado para um comando, a menos que esse comando seja exposto por meio de um item de menu.</span><span class="sxs-lookup"><span data-stu-id="c522b-108">The value of UI\_PKEY\_Keytip acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="c522b-109">Nesse caso, a estrutura ignora o valor da interface do usuário \_ PKEY \_ KeyTip e, em vez disso, usa um caractere precedido por um e comercial como especificado por [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou pelo [ \_ \_ rótulo de PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="c522b-109">In this case, the framework ignores the UI\_PKEY\_Keytip value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="c522b-110">Se nenhum e comercial for especificado pelo **comando Command. LabelTitle** ou UI \_ PKEY \_ , nenhum KeyTip ou acelerador de teclado será exposto.</span><span class="sxs-lookup"><span data-stu-id="c522b-110">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="c522b-111">O comprimento máximo da interface do usuário \_ PKEY \_ KeyTip é não associado.</span><span class="sxs-lookup"><span data-stu-id="c522b-111">The maximum length of UI\_PKEY\_Keytip is unbounded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c522b-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c522b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c522b-113">Propriedades do recurso</span><span class="sxs-lookup"><span data-stu-id="c522b-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="c522b-114">**Comando. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="c522b-114">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




