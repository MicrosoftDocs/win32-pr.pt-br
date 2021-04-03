---
title: UI_PKEY_Label
description: Identifica a \_ Propriedade do rótulo PKEY da interface do usuário \_ .
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245ce8d239e1a0893c907a047aa9a48996cbf606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822768"
---
# <a name="ui_pkey_label"></a><span data-ttu-id="931b3-103">\_Rótulo de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="931b3-103">UI\_PKEY\_Label</span></span>

<span data-ttu-id="931b3-104">Identifica a \_ Propriedade do rótulo PKEY da interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="931b3-104">Identifies the UI\_PKEY\_Label property.</span></span>

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="931b3-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="931b3-105">Remarks</span></span>

<span data-ttu-id="931b3-106">O rótulo PKEY da interface do usuário \_ \_ é usado por um aplicativo para consultar o texto do rótulo de guias, grupos, botões, itens da galeria e outros controles da faixa de tipos.</span><span class="sxs-lookup"><span data-stu-id="931b3-106">UI\_PKEY\_Label is used by an application to query the label text of tabs, groups, buttons, gallery items, and other Ribbon controls.</span></span>

> [!Note]  
> <span data-ttu-id="931b3-107">Windows 8 e mais recente: imagem do botão de [menu do aplicativo](windowsribbon-controls-applicationmenu.md) alterada para rótulo: **arquivo**.</span><span class="sxs-lookup"><span data-stu-id="931b3-107">Windows 8 and newer: [Application Menu](windowsribbon-controls-applicationmenu.md) button image changed to label: **File**.</span></span> <span data-ttu-id="931b3-108">Recomendamos que você não use o arquivo como rótulo para qualquer uma das suas próprias guias.</span><span class="sxs-lookup"><span data-stu-id="931b3-108">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

<span data-ttu-id="931b3-109">O valor da propriedade é uma cadeia de caracteres restrita a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="931b3-109">The property value is a string constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="931b3-110">Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="931b3-110">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="931b3-111">Não há suporte para alinhamento à direita.</span><span class="sxs-lookup"><span data-stu-id="931b3-111">Right alignment is not supported.</span></span>

<span data-ttu-id="931b3-112">O comprimento máximo do rótulo de PKEY da interface do usuário \_ \_ é não associado.</span><span class="sxs-lookup"><span data-stu-id="931b3-112">The maximum length of UI\_PKEY\_Label is unbounded.</span></span>

<span data-ttu-id="931b3-113">Se um comando for exposto por meio de um item de menu e o valor do rótulo [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou UI \_ PKEY \_ contiver uma letra precedida por um e comercial, conforme mostrado no exemplo a seguir, essa letra será tratada como um KeyTip e um acelerador de teclado para esse comando pela estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="931b3-113">If a Command is exposed through a menu item and the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or UI\_PKEY\_Label contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="931b3-114">Para exibir um e comercial em um rótulo, escape a designação de caractere especial com um e comercial duplo ( `&&` ), conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="931b3-114">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a><span data-ttu-id="931b3-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="931b3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="931b3-116">Propriedades do recurso</span><span class="sxs-lookup"><span data-stu-id="931b3-116">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="931b3-117">**Comando. LabelTitle**</span><span class="sxs-lookup"><span data-stu-id="931b3-117">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[<span data-ttu-id="931b3-118">\_LabelDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="931b3-118">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




