---
description: O conceito de linha evoluiu ao longo do tempo e foi parcialmente substituído pelos conceitos de endereço e terminal. A TAPI 3 não usa diretamente o conceito de linha, mas a TAPI 2 continua a incorporar esse paradigma.
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: Linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8275555e0cb34f5831ce671e22a89a1499fb1796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550516"
---
# <a name="line"></a>Linha

O conceito de linha evoluiu ao longo do tempo e foi parcialmente substituído pelos conceitos de endereço e terminal. A TAPI 3 não usa diretamente o conceito de linha, mas a TAPI 2 continua a incorporar esse paradigma.

Um *dispositivo de linha* é um dispositivo físico, como uma placa de fax, um modem ou uma placa ISDN que está conectada a uma rede. O dispositivo pode não estar fisicamente conectado ao computador no qual o aplicativo TAPI está sendo executado, como um pool de modems em um servidor. Os dispositivos de linha dão suporte a recursos de comunicação, permitindo que os aplicativos enviem informações ou recebam informações de uma rede. Um dispositivo de linha contém um conjunto de um ou mais canais homogêneos que podem ser usados para estabelecer chamadas.

Em aplicativos TAPI 2. x, um dispositivo de linha é a representação lógica de um dispositivo de telefone físico. Embora a "linha" sempre denotasse algo com dois pontos de extremidade, é possível abstrair um dispositivo de linha para um único ponto, pois a TAPI o exibe apenas como um ponto de entrada para a linha que leva à mudança.

![dispositivos de linha](images/ch0501.png)

Embora as três linhas na ilustração anterior sejam compostas de hardware diferente e usadas para funções diferentes, elas são abstratas para o mesmo tipo de dispositivo e governadas pelas mesmas regras. O telefone não representa um dispositivo de telefone, mas um dispositivo de linha usado para chamadas de voz. Ao usar esse dispositivo de linha para chamadas de entrada ou saída, o aplicativo também precisaria abrir e controlar uma instância da classe de dispositivo de telefone, que é descrita detalhadamente nas seções posteriores.

A classe de dispositivo line é uma representação independente de dispositivo de um dispositivo de linha física, como um modem. Ele pode conter um ou mais canais de comunicação idênticos (usados para sinalização e/ou informações) entre o aplicativo e o comutador ou a rede. Como os canais que pertencem a uma única linha têm recursos idênticos, eles são intercambiáveis. Em muitos casos (como com o POTS), um provedor de serviços modelará uma linha como tendo apenas um canal. Outras tecnologias, como o ISDN, oferecem mais canais e o provedor de serviços devem tratá-las adequadamente.

**TAPI 2. x:** Os aplicativos detectam recursos de linha usando a função [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) . A negociação de versão usando as funções [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) deve ter sido chamada anteriormente.

**TAPI 3. x:** Os aplicativos dependem principalmente do conceito de endereço.

 

 
