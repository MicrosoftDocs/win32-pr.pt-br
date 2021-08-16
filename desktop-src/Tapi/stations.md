---
description: Os conjuntos de estações que estão sendo monitorados por meio de um link de terceiros são modelados como um dispositivo de linha e, possivelmente, um dispositivo de telefone associado.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Estações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad9874542a63f05e124ea5df833aa0a433c03713cc3a2d7bb1ca3a471174e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760708"
---
# <a name="stations"></a>Estações

Os conjuntos de estações que estão sendo monitorados por meio de um link de terceiros são modelados como um dispositivo de linha e, possivelmente, um dispositivo de telefone associado. O dispositivo de linha poderá ter vários endereços, se o terminal modelado for compatível com mais de um DN (número de diretório). Várias aparências de chamada no mesmo DN podem ser modeladas como um único endereço que dá suporte a várias chamadas.

As chamadas entre duas estações na opção têm duas alças de chamada, uma dando a exibição de chamada da primeira estação (em seu dispositivo de linha) e a outra dando a exibição de chamada da segunda estação (em seu dispositivo de linha). Por exemplo, uma [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) de terceiros colocada por um aplicativo no servidor seria direcionada para o dispositivo de linha associado à estação da qual a chamada deve ser discada; uma alça de chamada seria criada nessa linha, no endereço especificado em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (dando controle sobre qual DN é usado em um telefone que dá suporte a vários DNs). Quando a chamada é oferecida para o endereço de destino, um novo manipular de chamada mostrando uma chamada no estado *de* oferta é criado; os aplicativos sabem que era outra exibição da mesma chamada pelo membro **dwCallID** em [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) sendo igual a ambas as chamadas. Ambas as chamadas seriam *ociosas* quando a chamada fosse retirada; uma chamada pode ser retirada do aplicativo de terceiros fazendo um [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) em qualquer um dos alças de chamada.

 

 



