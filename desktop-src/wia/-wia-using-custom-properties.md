---
description: Usando propriedades personalizadas.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Usando propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee01bc0df80acecec9805ea15cd8da65fa23a441c9c7818a88223aa47b963d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813626"
---
# <a name="using-custom-properties"></a>Usando propriedades personalizadas

**Usando propriedades personalizadas.**

Um Windows wia (aquisição de imagem) pode definir suas próprias propriedades personalizadas. Os chamadores podem manipular propriedades personalizadas da mesma forma que as propriedades de WIA normais. No entanto, somente seu aplicativo ou módulo de interface do usuário personalizado pode acessar essas propriedades personalizadas.

Os drivers WIA devem definir as propriedades personalizadas para ter identificadores de propriedade que são deslocadas pelo WIA PRIVATE DEVPROP para propriedades do dispositivo e usar WIA PRIVATE ITEMPROP para propriedades de item normais, como dentro \_ \_ de \_ \_ [IWiaMiniDrv::d rvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx). Para obter mais informações, consulte [Definindo propriedades personalizadas](-wia-defining-custom-properties.md).

Há duas maneiras de passar parâmetros personalizados para drivers WIA.

A primeira opção é usar o **método IWiaItemExtras::Escape** (descrito na documentação do SDK da Plataforma). Isso é semelhante ao [método IStiUSD::Escape,](https://msdn.microsoft.com/library/ms794396.aspx) mas permite que os chamadores usem o WIA diretamente, em vez de usar métodos DEIS. Usando **IWiaItemExtras::Escape**, você pode passar todas as informações para o driver e o driver pode passar todas as informações de volta. O serviço WIA gerencia apenas os buffers passados entre o chamador e o driver.

A segunda opção é usar propriedades personalizadas. Usar o método **IWiaItemExtras::Escape** é mais flexível do que usar propriedades WIA personalizadas, mas as propriedades personalizadas do WIA permitem que você armazene informações no fluxo de propriedades do item para que o driver possa ler as informações em outro momento.

 

 



