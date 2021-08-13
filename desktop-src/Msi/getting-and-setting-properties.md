---
description: Para usar propriedades em sua instalação, você pode obter e definir valores de propriedade de programas usando MsiGetProperty e MsiSetProperty e incluir como parte de instruções condicionais no banco de dados de instalação.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Obter e definir propriedades (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1009fc9370a870c53b3fe5ad471f52dea195648b36bab28dff76fe1271283be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635946"
---
# <a name="getting-and-setting-properties-windows-installer"></a>Obter e definir propriedades (Windows Instalador)

Para [](properties.md) usar propriedades em sua instalação, você pode obter e definir valores de propriedade de programas usando [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) e [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) e incluir como parte de instruções condicionais no banco de dados de instalação.

-   Para obter uma propriedade atual, chame a [**função MsiGetProperty.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)
-   Para obter o estado de instalação atual, chame a [**função MsiGetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)
-   Para obter o idioma para a instalação atual, chame a [**função MsiGetLanguage.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)
-   Para definir uma propriedade, chame a [**função MsiSetProperty.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)
-   Para definir o estado de instalação, chame a [**função MsiSetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)
-   Para limpar uma propriedade (definindo-a como Null), de definido o valor da propriedade como uma cadeia de caracteres vazia: "".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando propriedades](using-properties.md)
</dt> <dt>

[Definindo valores de propriedade pública na linha de comando](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Limpando uma propriedade do instalador](clearing-an-installer-property.md)
</dt> </dl>

 

 



