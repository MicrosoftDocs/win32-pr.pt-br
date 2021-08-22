---
description: Definindo propriedades personalizadas.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definindo propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b78516913c898e3b3d814e96a40d227cc3cc1cc70c13a290949f91eb9f447c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348046"
---
# <a name="defining-custom-properties"></a>Definindo propriedades personalizadas

**Definindo propriedades personalizadas**.

se for necessário para a minidriver de aquisição de imagem de Windows (WIA) definir propriedades personalizadas, a \_ \_ propriedade DEVPROP privada wia deverá ser usada para propriedades de item raiz personalizadas e a \_ propriedade de itemproperty privada do wia \_ deverá ser usada para outras propriedades de item. Essas constantes são definidas em *wiadef. h*.

O código de exemplo a seguir mostra definições para três propriedades de item raiz. A ID de propriedade da primeira propriedade de item raiz Personalizada, \_ prop raiz personalizada \_ \_ , 1, é definida em termos \_ de \_ DEVPROP privada WIA. As IDs de propriedade para propriedades adicionais do item raiz são definidas em termos de \_ DEVPROP privada WIA \_ + 1, WIA \_ privado \_ DEVPROP + 2 e assim por diante. O padrão pode ser continuado se forem necessárias propriedades de item raiz personalizadas adicionais.


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



O exemplo a seguir mostra definições para três propriedades de item filho personalizado e IDs de propriedade. A ID de propriedade da primeira propriedade de item filho personalizada, personalizada de \_ filho personalizado \_ \_ 1, é definida em termos de ItemProperty privada do WIA \_ \_ . As IDs de propriedade para propriedades de item filho adicionais são definidas em termos de \_ isprop particular do WIA \_ + 1 e assim por diante. Como antes, o padrão pode ser continuado se mais dessas propriedades personalizadas do item filho forem necessárias.


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



As propriedades de WIA personalizadas devem ter nomes de propriedade personalizada associados às IDs de propriedade personalizada. O código de exemplo a seguir mostra definições para três nomes de propriedade de item raiz personalizados. (Esses nomes de propriedade são usados com as IDs de propriedade personalizada que foram criadas em um exemplo anterior, em que o nome da propriedade personalizada contido em CUSTOM \_ \_ \_ A Str raiz prop 1 \_ é associada à raiz personalizada da ID de Propriedade do item raiz personalizado \_ \_ prop \_ 1.)


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> Os nomes de propriedade WIA *não* são localizados em vários idiomas. Isso ocorre porque as propriedades da WIA podem ser lidas por aplicativos que usam a ID da propriedade ou o nome da propriedade. Se o nome for usado, ele deve ser uma constante, assim como a ID de propriedade é.

 

 

 



