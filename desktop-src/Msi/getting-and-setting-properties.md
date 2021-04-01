---
description: Para usar as propriedades em sua instalação, você pode obter e definir valores de propriedade de programas usando MsiGetProperty e MsiSetProperty e incluir como parte das instruções condicionais no banco de dados de instalação.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Obtendo e definindo propriedades (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828994"
---
# <a name="getting-and-setting-properties-windows-installer"></a>Obtendo e definindo propriedades (Windows Installer)

Para usar [as propriedades](properties.md) em sua instalação, você pode obter e definir valores de propriedade de programas usando [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) e [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) e incluir como parte das instruções condicionais no banco de dados de instalação.

-   Para obter uma propriedade atual, chame a função [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .
-   Para obter o estado de instalação atual, chame a função [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .
-   Para obter o idioma para a instalação atual, chame a função [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .
-   Para definir uma propriedade, chame a função [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .
-   Para definir o estado de instalação, chame a função [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .
-   Para limpar uma propriedade (definindo-a como NULL), defina o valor da propriedade como uma cadeia de caracteres vazia: "".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando propriedades](using-properties.md)
</dt> <dt>

[Definindo valores de propriedade pública na linha de comando](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Limpando uma propriedade do instalador](clearing-an-installer-property.md)
</dt> </dl>

 

 



