---
title: Erro de TabIndex do ARIA
description: Erro de TabIndex do ARIA
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104008537"
---
# <a name="aria-tabindex-error"></a><span data-ttu-id="56e0b-104">Erro de TabIndex do ARIA</span><span class="sxs-lookup"><span data-stu-id="56e0b-104">ARIA Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="56e0b-105">Texto</span><span class="sxs-lookup"><span data-stu-id="56e0b-105">Text</span></span>

<span data-ttu-id="56e0b-106">O elemento não está desabilitado e tem um manipulador de eventos de **clique** , mas tem **TabIndex** < 0 e não está na ordem de tabulação por padrão.</span><span class="sxs-lookup"><span data-stu-id="56e0b-106">Element is not disabled and has a **click** event handler but it has **tabIndex** < 0 and is not in the tab order by default.</span></span>

## <a name="type"></a><span data-ttu-id="56e0b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="56e0b-107">Type</span></span>

<span data-ttu-id="56e0b-108">Erro</span><span class="sxs-lookup"><span data-stu-id="56e0b-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="56e0b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="56e0b-109">Description</span></span>

<span data-ttu-id="56e0b-110">Este erro se aplica a elementos que têm um manipulador de eventos de clique e não estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="56e0b-110">This error applies to elements that have a click event handler and are not disabled.</span></span> <span data-ttu-id="56e0b-111">Esses elementos devem estar na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="56e0b-111">These elements must be in the tab order.</span></span> <span data-ttu-id="56e0b-112">Isso garante que um elemento pode ser acessado usando a tecla Tab, que é como os usuários do leitor de tela normalmente navegam pela interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="56e0b-112">This ensures that an element can be reached using the Tab key, which is how screen reader users typically navigate the UI.</span></span>

<span data-ttu-id="56e0b-113">Para corrigir esse erro, defina o atributo [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) para um valor que seja igual ou maior que 0.</span><span class="sxs-lookup"><span data-stu-id="56e0b-113">To fix this error, set the [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) attribute to a value that is equal to or greater than 0.</span></span> <span data-ttu-id="56e0b-114">Você não precisa definir explicitamente o atributo **TabIndex** para as marcas que estão na ordem de tabulação por padrão, como [**um**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (com o atributo [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), o [**botão**](https://developer.mozilla.org/docs/Web/HTML/Element/button), a [**entrada**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluindo "oculto"), [**Select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**TextArea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)e [**Area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (como parte do mapa de imagem).</span><span class="sxs-lookup"><span data-stu-id="56e0b-114">You do not need to explicitly set the **tabindex** attribute for tags that are in the tab order by default, such as [**a**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (with [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) attribute), [**button**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluding "hidden"), [**select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea), and [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (as part of the image map).</span></span>

## <a name="example"></a><span data-ttu-id="56e0b-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="56e0b-115">Example</span></span>


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




