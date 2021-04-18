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
# <a name="userslanguage-control-attribute"></a>Atributo de controle UsersLanguage

Se esse sinalizador de bit for definido, as fontes serão criadas usando a página de código padrão da interface do usuário. Se o sinalizador de bit não for definido, as fontes serão criadas usando a página de código do banco de dados.

## <a name="valid-controls"></a>Controles válidos

[Text](text-control.md)

 

[ListBox](listbox-control.md)

 

[ComboBox](combobox-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 1048576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

## <a name="remarks"></a>Comentários

Esse atributo de controle pode ser usado para exibir o texto que o usuário inseriu em um controle de [edição](edit-control.md) ou [PathEdit](pathedit-control.md) .

O controle de edição, o controle PathEdit, o controle [directorylist](directorylist-control.md) e o [controle DirectoryCombo](directorycombo-control.md) sempre usam as fontes criadas na página de código padrão da interface do usuário. Isso pode causar problemas se idiomas adicionais tiverem sido instalados no sistema operacional. Nesse caso, as fontes no computador podem não ser capazes de representar todos os caracteres nos idiomas adicionados. Para determinar quais fontes podem ser usadas, pesquise os valores em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SYSTEMLINK**.

Para obter mais informações, consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



