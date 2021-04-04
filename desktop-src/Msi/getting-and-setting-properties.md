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
# <a name="getting-and-setting-properties-windows-installer"></a><span data-ttu-id="f6ba6-103">Obtendo e definindo propriedades (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="f6ba6-103">Getting and Setting Properties (Windows Installer)</span></span>

<span data-ttu-id="f6ba6-104">Para usar [as propriedades](properties.md) em sua instalação, você pode obter e definir valores de propriedade de programas usando [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) e [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) e incluir como parte das instruções condicionais no banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="f6ba6-104">To use [properties](properties.md) in your installation, you can get and set property values from programs using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) and [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) and include as part of conditional statements in the installation database.</span></span>

-   <span data-ttu-id="f6ba6-105">Para obter uma propriedade atual, chame a função [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="f6ba6-105">To obtain a current property, call the [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) function.</span></span>
-   <span data-ttu-id="f6ba6-106">Para obter o estado de instalação atual, chame a função [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .</span><span class="sxs-lookup"><span data-stu-id="f6ba6-106">To obtain the current installation state, call the [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function.</span></span>
-   <span data-ttu-id="f6ba6-107">Para obter o idioma para a instalação atual, chame a função [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) .</span><span class="sxs-lookup"><span data-stu-id="f6ba6-107">To obtain the language for the current installation, call the [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) function.</span></span>
-   <span data-ttu-id="f6ba6-108">Para definir uma propriedade, chame a função [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) .</span><span class="sxs-lookup"><span data-stu-id="f6ba6-108">To set a property, call the [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) function.</span></span>
-   <span data-ttu-id="f6ba6-109">Para definir o estado de instalação, chame a função [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) .</span><span class="sxs-lookup"><span data-stu-id="f6ba6-109">To set the installation state, call the [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) function.</span></span>
-   <span data-ttu-id="f6ba6-110">Para limpar uma propriedade (definindo-a como NULL), defina o valor da propriedade como uma cadeia de caracteres vazia: "".</span><span class="sxs-lookup"><span data-stu-id="f6ba6-110">To clear a property (setting it to Null), set the property's value to an empty string: "".</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6ba6-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6ba6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6ba6-112">Usando propriedades</span><span class="sxs-lookup"><span data-stu-id="f6ba6-112">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="f6ba6-113">Definindo valores de propriedade pública na linha de comando</span><span class="sxs-lookup"><span data-stu-id="f6ba6-113">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="f6ba6-114">Limpando uma propriedade do instalador</span><span class="sxs-lookup"><span data-stu-id="f6ba6-114">Clearing an Installer Property</span></span>](clearing-an-installer-property.md)
</dt> </dl>

 

 



