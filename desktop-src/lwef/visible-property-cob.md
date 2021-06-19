---
title: Propriedade Visible (objeto Characters)
description: Saiba mais sobre a Propriedade Visível do objeto Characters, que retorna um booliana que indica se o caractere está visível.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396301"
---
# <a name="visible-property-characters-object"></a><span data-ttu-id="8d16a-103">Propriedade Visible (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="8d16a-103">Visible Property (Characters Object)</span></span>

<span data-ttu-id="8d16a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8d16a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8d16a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8d16a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8d16a-106">Retorna um booliana que indica se o caractere está visível.</span><span class="sxs-lookup"><span data-stu-id="8d16a-106">Returns a Boolean indicating whether the character is visible.</span></span>

</dd> <dt>

<span data-ttu-id="8d16a-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="8d16a-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="8d16a-108">*agent\***. Characters(**"* CharacterID *"\*\*). Visível*\*</span><span class="sxs-lookup"><span data-stu-id="8d16a-108">*agent\***.Characters(**"* CharacterID *"\*\*).Visible*\*</span></span>



| <span data-ttu-id="8d16a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="8d16a-109">Value</span></span> | <span data-ttu-id="8d16a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d16a-110">Description</span></span>                            |
|-------|----------------------------------------|
| <span data-ttu-id="8d16a-111">True</span><span class="sxs-lookup"><span data-stu-id="8d16a-111">True</span></span>  | <span data-ttu-id="8d16a-112">O caractere é exibido.</span><span class="sxs-lookup"><span data-stu-id="8d16a-112">The character is displayed.</span></span>            |
| <span data-ttu-id="8d16a-113">Falso</span><span class="sxs-lookup"><span data-stu-id="8d16a-113">False</span></span> | <span data-ttu-id="8d16a-114">O caractere está oculto (não visível).</span><span class="sxs-lookup"><span data-stu-id="8d16a-114">The character is hidden (not visible).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d16a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d16a-115">Remarks</span></span>

<span data-ttu-id="8d16a-116">Essa propriedade indica se o quadro do caractere está sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="8d16a-116">This property indicates whether the character's frame is being displayed.</span></span> <span data-ttu-id="8d16a-117">Isso não significa necessariamente que há uma imagem na tela.</span><span class="sxs-lookup"><span data-stu-id="8d16a-117">It does not necessarily mean that there is an image on the screen.</span></span> <span data-ttu-id="8d16a-118">Por exemplo, essa propriedade retorna **True** mesmo quando o caractere é posicionado fora da área de exibição visível ou quando o quadro de caracteres atual não contém imagens.</span><span class="sxs-lookup"><span data-stu-id="8d16a-118">For example, this property returns **True** even when the character is positioned off the visible display area or when the current character frame contains no images.</span></span> <span data-ttu-id="8d16a-119">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="8d16a-119">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="8d16a-120">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8d16a-120">This property is read-only.</span></span> <span data-ttu-id="8d16a-121">Para tornar um caractere visível ou oculto, use os [**métodos Show**](show-method.md) ou [**Hide.**](https://www.bing.com/search?q=**Hide**)</span><span class="sxs-lookup"><span data-stu-id="8d16a-121">To make a character visible or hidden, use the [**Show**](show-method.md) or [**Hide**](https://www.bing.com/search?q=**Hide**) methods.</span></span>

 

 




