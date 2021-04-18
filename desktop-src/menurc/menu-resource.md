---
title: Recurso de MENU
description: Define o conteúdo de um recurso de menu. | Recurso de MENU
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menus de recursos de MENU e outros recursos
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105787685"
---
# <a name="menu-resource"></a><span data-ttu-id="a592e-105">Recurso de MENU</span><span class="sxs-lookup"><span data-stu-id="a592e-105">MENU resource</span></span>

<span data-ttu-id="a592e-106">Define o conteúdo de um recurso de menu.</span><span class="sxs-lookup"><span data-stu-id="a592e-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="a592e-107">Um recurso de menu é uma coleção de informações que define a aparência e a função de um menu de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a592e-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="a592e-108">Um menu é uma ferramenta de entrada especial que permite que um usuário selecione comandos e abra submenus de uma lista de itens de menu.</span><span class="sxs-lookup"><span data-stu-id="a592e-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span>

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a><span data-ttu-id="a592e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a592e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a592e-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menu de atalho*</span><span class="sxs-lookup"><span data-stu-id="a592e-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span></span>
</dt> <dd>

<span data-ttu-id="a592e-111">Número que identifica o menu.</span><span class="sxs-lookup"><span data-stu-id="a592e-111">Number that identifies the menu.</span></span> <span data-ttu-id="a592e-112">Esse valor é uma cadeia de caracteres exclusiva ou um valor inteiro não assinado de 16 bits no intervalo de 1 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="a592e-112">This value is either a unique string or a unique 16-bit unsigned integer value in the range of 1 to 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="a592e-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*</span><span class="sxs-lookup"><span data-stu-id="a592e-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="a592e-114">Esse parâmetro pode ser zero de mais das instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="a592e-114">This parameter can be zero of more of the following statements.</span></span>



| <span data-ttu-id="a592e-115">Instrução</span><span class="sxs-lookup"><span data-stu-id="a592e-115">Statement</span></span>                                                        | <span data-ttu-id="a592e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a592e-116">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a592e-117">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="a592e-117">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="a592e-118">Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="a592e-118">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="a592e-119">Para obter mais informações, consulte [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="a592e-119">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="a592e-120">[](language-statement.md) *Idioma* do idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="a592e-120">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="a592e-121">Idioma do recurso.</span><span class="sxs-lookup"><span data-stu-id="a592e-121">Language for the resource.</span></span> <span data-ttu-id="a592e-122">Para obter mais informações, consulte [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="a592e-122">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="a592e-123">[](version-statement.md) *DWORD* da versão</span><span class="sxs-lookup"><span data-stu-id="a592e-123">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="a592e-124">Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="a592e-124">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="a592e-125">Para obter mais informações, consulte [**versão**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="a592e-125">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> </dl>

<span data-ttu-id="a592e-126">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a592e-126">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="a592e-127">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a592e-127">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a592e-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a592e-128">Examples</span></span>

<span data-ttu-id="a592e-129">Veja a seguir um exemplo de uma instrução de **menu** completa:</span><span class="sxs-lookup"><span data-stu-id="a592e-129">The following is an example of a complete **MENU** statement:</span></span>

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a><span data-ttu-id="a592e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a592e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a592e-131">Uso de Menus</span><span class="sxs-lookup"><span data-stu-id="a592e-131">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="a592e-132">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="a592e-132">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="a592e-133">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="a592e-133">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="a592e-134">**IDIOMA**</span><span class="sxs-lookup"><span data-stu-id="a592e-134">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="a592e-135">**MENUEX**</span><span class="sxs-lookup"><span data-stu-id="a592e-135">**MENUEX**</span></span>](menuex-resource.md)
</dt> <dt>

[<span data-ttu-id="a592e-136">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="a592e-136">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="a592e-137">**POP-up**</span><span class="sxs-lookup"><span data-stu-id="a592e-137">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="a592e-138">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="a592e-138">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="a592e-139">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="a592e-139">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="a592e-140">**Versão**</span><span class="sxs-lookup"><span data-stu-id="a592e-140">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
