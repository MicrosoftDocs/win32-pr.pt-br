---
description: O Unimodem, ou driver de modem universal, TSP (Unimdm. TSP) fornece acesso a quase todos os modems padrão.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4562ad7692c288a963db27b6859fa5c472d8ff80017e2726c277fbf9d24452be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011896"
---
# <a name="unimodem-tsp"></a>Unimodem TSP

O Unimodem, ou driver de modem universal, TSP (Unimdm. TSP) fornece acesso a quase todos os modems padrão. Ele dá suporte a modems de voz que permitem streaming Half-duplex. Eles são compatíveis com o Wave MSP e o controle de fluxo é possível. (observe que o unimodem no Windows NT 4,0 ou anterior não dá suporte a modems de voz, portanto, o controle direto de fluxo não é possível.)

Este TSP dá suporte a um valor de [**tipo de endereço**](./lineaddresstype--constants.md) de LINEADDRESSTYPE \_ PHONENUMBER. Se o programador quiser usar as regras de discagem, a interface TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) ou a função TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) deverá ser usada para obter uma cadeia de caracteres discáveis de um número de telefone em formato canônico.

o unimodem TSP é instalado com os sistemas operacionais Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 e Windows 95.

 

 
