---
description: Usando propriedades personalizadas.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Usando propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811466"
---
# <a name="using-custom-properties"></a>Usando propriedades personalizadas

**Usando propriedades personalizadas**.

Um driver WIA (aquisição de imagem do Windows) pode definir suas próprias propriedades personalizadas. Os chamadores podem manipular propriedades personalizadas assim como as propriedades de WIA normais. No entanto, somente seu aplicativo ou módulo de interface do usuário personalizada pode acessar essas propriedades personalizadas.

Os drivers WIA devem definir as propriedades personalizadas para que os identificadores de propriedade sejam deslocados pelo \_ \_ DEVPROP privado do WIA para as propriedades do dispositivo e usem \_ o ItemProperty privado do WIA \_ para propriedades normais do item, como dentro de [IWiaMiniDrv::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx). Para obter mais informações, consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md).

Há duas maneiras de passar parâmetros personalizados para drivers WIA.

A primeira opção é usar o método **IWiaItemExtras:: escape** (descrito na documentação do Platform SDK). Isso é semelhante ao método [IStiUSD:: escape](https://msdn.microsoft.com/library/ms794396.aspx) , mas permite que os chamadores usem o WIA diretamente, em vez de usar métodos STI. Usando **IWiaItemExtras:: escape**, você pode passar todas as informações para o driver e o driver pode passar qualquer informação de volta. O serviço WIA gerencia somente os buffers passados entre o chamador e o driver.

A segunda opção é usar propriedades personalizadas. O uso do método **IWiaItemExtras:: escape** é mais flexível do que o uso de propriedades WIA personalizadas, mas as propriedades WIA personalizadas permitem que você armazene informações no fluxo de propriedades do item para que o driver possa ler as informações em outro momento.

 

 



