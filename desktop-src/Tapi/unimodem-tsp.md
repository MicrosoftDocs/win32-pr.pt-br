---
description: O Unimodem, ou driver de modem universal, TSP (Unimdm. TSP) fornece acesso a quase todos os modems padrão.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761342"
---
# <a name="unimodem-tsp"></a>Unimodem TSP

O Unimodem, ou driver de modem universal, TSP (Unimdm. TSP) fornece acesso a quase todos os modems padrão. Ele dá suporte a modems de voz que permitem streaming Half-duplex. Eles são compatíveis com o Wave MSP e o controle de fluxo é possível. (Observe que o Unimodem no Windows NT 4,0 ou anterior não dá suporte a modems de voz, portanto, o controle direto de fluxo não é possível.)

Este TSP dá suporte a um valor de [**tipo de endereço**](./lineaddresstype--constants.md) de LINEADDRESSTYPE \_ PHONENUMBER. Se o programador quiser usar as regras de discagem, a interface TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) ou a função TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) deverá ser usada para obter uma cadeia de caracteres discáveis de um número de telefone em formato canônico.

O Unimodem TSP é instalado com sistemas operacionais Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 e Windows 95.

 

 
