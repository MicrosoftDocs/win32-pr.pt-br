---
title: Propriedade Visible (objeto characters)
description: Propriedade Visible
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105813305"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="e15cd-103">Propriedade Visible (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="e15cd-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="e15cd-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e15cd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e15cd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="e15cd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e15cd-106">Retorna um valor booleano que indica se o caractere está visível.</span><span class="sxs-lookup"><span data-stu-id="e15cd-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="e15cd-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="e15cd-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="e15cd-108">\*agente \***. Caracteres (**"\* characterid *" \* *). Visível**</span><span class="sxs-lookup"><span data-stu-id="e15cd-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="e15cd-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e15cd-109">Value</span></span> | <span data-ttu-id="e15cd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e15cd-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="e15cd-111">True</span><span class="sxs-lookup"><span data-stu-id="e15cd-111">True</span></span>  | <span data-ttu-id="e15cd-112">O caractere é exibido.</span><span class="sxs-lookup"><span data-stu-id="e15cd-112">The character is displayed.</span></span>            |
| <span data-ttu-id="e15cd-113">Falso</span><span class="sxs-lookup"><span data-stu-id="e15cd-113">False</span></span> | <span data-ttu-id="e15cd-114">O caractere é oculto (não visível).</span><span class="sxs-lookup"><span data-stu-id="e15cd-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e15cd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e15cd-115">Remarks</span></span>

<span data-ttu-id="e15cd-116">Esta propriedade indica se o quadro do caractere está sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="e15cd-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="e15cd-117">Isso não significa necessariamente que há uma imagem na tela.</span><span class="sxs-lookup"><span data-stu-id="e15cd-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="e15cd-118">Por exemplo, essa propriedade retorna **true** mesmo quando o caractere é posicionado fora da área de exibição visível ou quando o quadro de caracteres atual não contém nenhuma imagem.</span><span class="sxs-lookup"><span data-stu-id="e15cd-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="e15cd-119">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="e15cd-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="e15cd-120">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e15cd-120">This property is read-only.</span></span> <span data-ttu-id="e15cd-121">Para tornar um caractere visível ou oculto, use os métodos [**show**](show-method.md) ou [**Hide**](https://www.bing.com/search?q=**Hide**) .</span><span class="sxs-lookup"><span data-stu-id="e15cd-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




