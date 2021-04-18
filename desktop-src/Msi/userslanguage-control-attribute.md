---
description: Se esse sinalizador de bit for definido, as fontes serão criadas usando a página de código padrão da interface do usuário. Se o sinalizador de bit não for definido, as fontes serão criadas usando a página de código do banco de dados.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Atributo de controle UsersLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779620"
---
# <a name="userslanguage-control-attribute"></a><span data-ttu-id="4afc9-104">Atributo de controle UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="4afc9-104">UsersLanguage Control Attribute</span></span>

<span data-ttu-id="4afc9-105">Se esse sinalizador de bit for definido, as fontes serão criadas usando a página de código padrão da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4afc9-105">If this bit flag is set, fonts are created using the user's default UI code page.</span></span> <span data-ttu-id="4afc9-106">Se o sinalizador de bit não for definido, as fontes serão criadas usando a página de código do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4afc9-106">If the bit flag is not set, fonts are created using the database code page.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="4afc9-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="4afc9-107">Valid Controls</span></span>

[<span data-ttu-id="4afc9-108">Text</span><span class="sxs-lookup"><span data-stu-id="4afc9-108">Text</span></span>](text-control.md)

 

[<span data-ttu-id="4afc9-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="4afc9-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="4afc9-110">ComboBox</span><span class="sxs-lookup"><span data-stu-id="4afc9-110">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="4afc9-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4afc9-111">Value</span></span>



| <span data-ttu-id="4afc9-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="4afc9-112">Decimal</span></span> | <span data-ttu-id="4afc9-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="4afc9-113">Hexadecimal</span></span> | <span data-ttu-id="4afc9-114">Constante</span><span class="sxs-lookup"><span data-stu-id="4afc9-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="4afc9-115">1048576</span><span class="sxs-lookup"><span data-stu-id="4afc9-115">1048576</span></span> | <span data-ttu-id="4afc9-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="4afc9-116">0x00100000</span></span>  | <span data-ttu-id="4afc9-117">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="4afc9-117">**msidbControlAttributesUsersLanguage**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4afc9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4afc9-118">Remarks</span></span>

<span data-ttu-id="4afc9-119">Esse atributo de controle pode ser usado para exibir o texto que o usuário inseriu em um controle de [edição](edit-control.md) ou [PathEdit](pathedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="4afc9-119">This control attribute can be used to display text that the user has entered into an [Edit](edit-control.md) or [PathEdit](pathedit-control.md) control.</span></span>

<span data-ttu-id="4afc9-120">O controle de edição, o controle PathEdit, o controle [directorylist](directorylist-control.md) e o [controle DirectoryCombo](directorycombo-control.md) sempre usam as fontes criadas na página de código padrão da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4afc9-120">The Edit control, PathEdit control, [DirectoryList control](directorylist-control.md) and [DirectoryCombo control](directorycombo-control.md) always use the fonts created in the user's default UI code page.</span></span> <span data-ttu-id="4afc9-121">Isso pode causar problemas se idiomas adicionais tiverem sido instalados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4afc9-121">This can cause problems if additional languages have been installed on the operating system.</span></span> <span data-ttu-id="4afc9-122">Nesse caso, as fontes no computador podem não ser capazes de representar todos os caracteres nos idiomas adicionados.</span><span class="sxs-lookup"><span data-stu-id="4afc9-122">In this case, the fonts on the computer may not be able to represent all the characters in the added languages.</span></span> <span data-ttu-id="4afc9-123">Para determinar quais fontes podem ser usadas, pesquise os valores em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SYSTEMLINK**.</span><span class="sxs-lookup"><span data-stu-id="4afc9-123">To determine what fonts can be used, look up the values in **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\FontLink\\SystemLink**.</span></span>

<span data-ttu-id="4afc9-124">Para obter mais informações, consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="4afc9-124">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



