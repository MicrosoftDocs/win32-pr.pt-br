---
description: Definindo propriedades personalizadas.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definindo propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781633"
---
# <a name="defining-custom-properties"></a><span data-ttu-id="d47ae-103">Definindo propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="d47ae-103">Defining Custom Properties</span></span>

<span data-ttu-id="d47ae-104">**Definindo propriedades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="d47ae-104">**Defining Custom Properties**.</span></span>

<span data-ttu-id="d47ae-105">Se for necessário que o minidriver da aquisição de imagens do Windows (WIA) defina propriedades personalizadas, a \_ \_ Propriedade DEVPROP privada WIA deverá ser usada para propriedades de item raiz personalizadas e a \_ propriedade de ItemProperty particular do WIA \_ deverá ser usada para outras propriedades de item.</span><span class="sxs-lookup"><span data-stu-id="d47ae-105">If it is necessary for the Windows Image Acquisition (WIA) minidriver to define custom properties, the WIA\_PRIVATE\_DEVPROP property should be used for custom root item properties, and the WIA\_PRIVATE\_ITEMPROP" property should be used for other item properties.</span></span> <span data-ttu-id="d47ae-106">Essas constantes são definidas em *wiadef. h*.</span><span class="sxs-lookup"><span data-stu-id="d47ae-106">These constants are defined in *wiadef.h*.</span></span>

<span data-ttu-id="d47ae-107">O código de exemplo a seguir mostra definições para três propriedades de item raiz.</span><span class="sxs-lookup"><span data-stu-id="d47ae-107">The following example code shows definitions for three root item properties.</span></span> <span data-ttu-id="d47ae-108">A ID de propriedade da primeira propriedade de item raiz Personalizada, \_ prop raiz personalizada \_ \_ , 1, é definida em termos \_ de \_ DEVPROP privada WIA.</span><span class="sxs-lookup"><span data-stu-id="d47ae-108">The property ID for the first custom root item property, CUSTOM\_ROOT\_PROP\_1, is defined in terms of WIA\_PRIVATE\_DEVPROP.</span></span> <span data-ttu-id="d47ae-109">As IDs de propriedade para propriedades adicionais do item raiz são definidas em termos de \_ DEVPROP privada WIA \_ + 1, WIA \_ privado \_ DEVPROP + 2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d47ae-109">Property IDs for additional root item properties are defined in terms of WIA\_PRIVATE\_DEVPROP + 1, WIA\_PRIVATE\_DEVPROP + 2, and so on.</span></span> <span data-ttu-id="d47ae-110">O padrão pode ser continuado se forem necessárias propriedades de item raiz personalizadas adicionais.</span><span class="sxs-lookup"><span data-stu-id="d47ae-110">The pattern can be continued if additional custom root item properties are needed.</span></span>


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



<span data-ttu-id="d47ae-111">O exemplo a seguir mostra definições para três propriedades de item filho personalizado e IDs de propriedade.</span><span class="sxs-lookup"><span data-stu-id="d47ae-111">The next example shows definitions for three custom child item properties and property IDs.</span></span> <span data-ttu-id="d47ae-112">A ID de propriedade da primeira propriedade de item filho personalizada, personalizada de \_ filho personalizado \_ \_ 1, é definida em termos de ItemProperty privada do WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d47ae-112">The property ID for the first custom child item property, CUSTOM\_CHILD\_PROP\_1, is defined in terms of WIA\_PRIVATE\_ITEMPROP.</span></span> <span data-ttu-id="d47ae-113">As IDs de propriedade para propriedades de item filho adicionais são definidas em termos de \_ isprop particular do WIA \_ + 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d47ae-113">Property IDs for additional child item properties are defined in terms of WIA\_PRIVATE\_ITEMPROP + 1, and so on.</span></span> <span data-ttu-id="d47ae-114">Como antes, o padrão pode ser continuado se mais dessas propriedades personalizadas do item filho forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="d47ae-114">As before, the pattern can be continued if more of these custom child item properties are needed.</span></span>


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



<span data-ttu-id="d47ae-115">As propriedades de WIA personalizadas devem ter nomes de propriedade personalizada associados às IDs de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="d47ae-115">Custom WIA properties must have custom property names that are associated with the custom property IDs.</span></span> <span data-ttu-id="d47ae-116">O código de exemplo a seguir mostra definições para três nomes de propriedade de item raiz personalizados.</span><span class="sxs-lookup"><span data-stu-id="d47ae-116">The following example code shows definitions for three custom root item property names.</span></span> <span data-ttu-id="d47ae-117">(Esses nomes de propriedade são usados com as IDs de propriedade personalizada que foram criadas em um exemplo anterior, em que o nome da propriedade personalizada contido em CUSTOM \_ \_ \_ A Str raiz prop 1 \_ é associada à raiz personalizada da ID de Propriedade do item raiz personalizado \_ \_ prop \_ 1.)</span><span class="sxs-lookup"><span data-stu-id="d47ae-117">(These property names are used with the custom property IDs that were created in a previous example, where the custom property name contained in CUSTOM\_ROOT\_PROP\_1\_STR is associated with the custom root item property ID CUSTOM\_ROOT\_PROP\_1.)</span></span>


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> <span data-ttu-id="d47ae-118">Os nomes de propriedade WIA *não* são localizados em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="d47ae-118">WIA property names are *not* localized in multiple languages.</span></span> <span data-ttu-id="d47ae-119">Isso ocorre porque as propriedades da WIA podem ser lidas por aplicativos que usam a ID da propriedade ou o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d47ae-119">This is because WIA properties can be read by applications using the property ID or the property name.</span></span> <span data-ttu-id="d47ae-120">Se o nome for usado, ele deve ser uma constante, assim como a ID de propriedade é.</span><span class="sxs-lookup"><span data-stu-id="d47ae-120">If the name is used, it must be a constant, just as the property ID is.</span></span>

 

 

 



