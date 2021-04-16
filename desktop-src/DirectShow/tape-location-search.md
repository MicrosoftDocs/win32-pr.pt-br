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
# <a name="tape-location-search"></a><span data-ttu-id="aec62-103">Pesquisa de local de fita</span><span class="sxs-lookup"><span data-stu-id="aec62-103">Tape Location Search</span></span>

<span data-ttu-id="aec62-104">Embora os dispositivos DV ofereçam suporte a um comando para pesquisar por código de tempo ou por número de faixa absoluta (ATN), o driver MSDV não tem uma maneira padrão e independente de dispositivo de acessar essas funções.</span><span class="sxs-lookup"><span data-stu-id="aec62-104">Although DV devices support a command to search by time code or by absolute track number (ATN), the MSDV driver does not have a standard, device-independent way to access these functions.</span></span> <span data-ttu-id="aec62-105">A única opção é enviar um comando AV/C bruto para o driver, conforme descrito no tópico [emitindo comandos Av/c brutos](issuing-raw-av-c-commands.md).</span><span class="sxs-lookup"><span data-stu-id="aec62-105">The only option is to send a raw AV/C command to the driver as described in the topic [Issuing Raw AV/C Commands](issuing-raw-av-c-commands.md).</span></span>

<span data-ttu-id="aec62-106">O driver UVC dá suporte a uma propriedade definida para pesquisas de local de fita.</span><span class="sxs-lookup"><span data-stu-id="aec62-106">The UVC driver supports a property set for tape location searches.</span></span> <span data-ttu-id="aec62-107">Para enviar um comando de pesquisa, use a interface **IKsControl** e defina a propriedade de transporte propsetid \_ ext \_ .</span><span class="sxs-lookup"><span data-stu-id="aec62-107">To send a search command, use the **IKsControl** interface and set the PROPSETID\_EXT\_TRANSPORT property.</span></span> <span data-ttu-id="aec62-108">O uso de um conjunto de propriedades é mais seguro do que o envio de comandos AV/C brutos para o dispositivo, pois os comandos AV/C ignoram o filtro e vão diretamente para o driver do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aec62-108">Using a property set is safer than sending raw AV/C commands to the device, because AV/C commands bypass the filter and go directly to the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aec62-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aec62-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec62-110">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="aec62-110">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="aec62-111">Conjunto de propriedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="aec62-111">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



