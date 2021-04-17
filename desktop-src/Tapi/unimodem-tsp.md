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
# <a name="unimodem-tsp"></a><span data-ttu-id="a6a62-103">Unimodem TSP</span><span class="sxs-lookup"><span data-stu-id="a6a62-103">Unimodem TSP</span></span>

<span data-ttu-id="a6a62-104">O Unimodem, ou driver de modem universal, TSP (Unimdm. TSP) fornece acesso a quase todos os modems padrão.</span><span class="sxs-lookup"><span data-stu-id="a6a62-104">The Unimodem, or Universal Modem Driver, TSP (Unimdm.tsp) provides access to nearly all standard modems.</span></span> <span data-ttu-id="a6a62-105">Ele dá suporte a modems de voz que permitem streaming Half-duplex.</span><span class="sxs-lookup"><span data-stu-id="a6a62-105">It supports voice modems that allow half-duplex streaming.</span></span> <span data-ttu-id="a6a62-106">Eles são compatíveis com o Wave MSP e o controle de fluxo é possível.</span><span class="sxs-lookup"><span data-stu-id="a6a62-106">They are supported by the Wave MSP and stream control is possible.</span></span> <span data-ttu-id="a6a62-107">(Observe que o Unimodem no Windows NT 4,0 ou anterior não dá suporte a modems de voz, portanto, o controle direto de fluxo não é possível.)</span><span class="sxs-lookup"><span data-stu-id="a6a62-107">(Note that Unimodem on Windows NT 4.0 or earlier does not support voice modems, so direct stream control is not possible.)</span></span>

<span data-ttu-id="a6a62-108">Este TSP dá suporte a um valor de [**tipo de endereço**](./lineaddresstype--constants.md) de LINEADDRESSTYPE \_ PHONENUMBER.</span><span class="sxs-lookup"><span data-stu-id="a6a62-108">This TSP supports an [**address type**](./lineaddresstype--constants.md) value of LINEADDRESSTYPE\_PHONENUMBER.</span></span> <span data-ttu-id="a6a62-109">Se o programador quiser usar as regras de discagem, a interface TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) ou a função TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) deverá ser usada para obter uma cadeia de caracteres discáveis de um número de telefone em formato canônico.</span><span class="sxs-lookup"><span data-stu-id="a6a62-109">If the programmer wants to use the dialing rules, the TAPI 3 [**ITAddressTranslation**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) interface or the TAPI 2 [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) function must be used to obtain a dialable string from a phone number in canonical format.</span></span>

<span data-ttu-id="a6a62-110">O Unimodem TSP é instalado com sistemas operacionais Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="a6a62-110">The Unimodem TSP is installed with Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98, and Windows 95.</span></span>

 

 
