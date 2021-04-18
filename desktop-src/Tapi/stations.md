---
description: Os conjuntos de estações sendo monitorados por meio de um link de terceiros são modelados como um dispositivo de linha e, possivelmente, um dispositivo de telefone associado.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Rádio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810994"
---
# <a name="stations"></a>Rádio

Os conjuntos de estações sendo monitorados por meio de um link de terceiros são modelados como um dispositivo de linha e, possivelmente, um dispositivo de telefone associado. O dispositivo de linha pode ter vários endereços, se o terminal modelado der suporte a mais de um DN (número de diretório). Várias aparências de chamada no mesmo DN podem ser modeladas como um único endereço que dá suporte a várias chamadas.

As chamadas entre duas estações no comutador têm dois identificadores de chamada, um fornecendo a exibição de chamada da primeira estação (em seu dispositivo de linha) e o outro que dá a exibição de chamada da segunda estação (em seu dispositivo de linha). Por exemplo, um [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) de terceiros colocado por um aplicativo no servidor seria direcionado para o dispositivo de linha associado à estação da qual a chamada será discada; um identificador de chamada seria criado nessa linha, no endereço especificado em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (permitindo assim o controle sobre qual DN é usado em um telefone que dá suporte a vários DNS). Quando a chamada é oferecida ao endereço de destino, um novo identificador de chamada mostrando uma chamada no estado de *oferta* é criado; os aplicativos sabem que era outra exibição da mesma chamada pelo membro **dwCallID** em [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) sendo igual para ambas as chamadas. Ambas as chamadas ficarão *ociosas* quando a chamada fosse descartada; uma chamada pode ser descartada do aplicativo de terceiros fazendo um [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) em qualquer um dos identificadores de chamada.

 

 



