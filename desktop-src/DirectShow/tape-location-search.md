---
description: Pesquisa de local de fita
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Pesquisa de local de fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758046"
---
# <a name="tape-location-search"></a>Pesquisa de local de fita

Embora os dispositivos DV ofereçam suporte a um comando para pesquisar por código de tempo ou por número de faixa absoluta (ATN), o driver MSDV não tem uma maneira padrão e independente de dispositivo de acessar essas funções. A única opção é enviar um comando AV/C bruto para o driver, conforme descrito no tópico [emitindo comandos Av/c brutos](issuing-raw-av-c-commands.md).

O driver UVC dá suporte a uma propriedade definida para pesquisas de local de fita. Para enviar um comando de pesquisa, use a interface **IKsControl** e defina a propriedade de transporte propsetid \_ ext \_ . O uso de um conjunto de propriedades é mais seguro do que o envio de comandos AV/C brutos para o dispositivo, pois os comandos AV/C ignoram o filtro e vão diretamente para o driver do dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Conjunto de propriedades de transporte de dispositivo externo](external-device-transport-property-set.md)
</dt> </dl>

 

 



