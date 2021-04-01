---
description: As operações de discagem permitem que um aplicativo envie dígitos adicionais em uma sessão criada anteriormente. Um exemplo de uso de discagem parcial é discar uma extensão. A discagem parcial é, às vezes, chamada de discagem incremental ou discagem atrasada.
ms.assetid: 1dfaefd7-f8dd-451e-af18-249c89bdb517
title: Discagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c603d8e846694b4728d1b5ad4c887be34fbac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646969"
---
# <a name="dial"></a>Discagem

As operações de discagem permitem que um aplicativo envie dígitos adicionais em uma sessão criada anteriormente. Um exemplo de uso de discagem parcial é discar uma extensão. A discagem parcial é, às vezes, chamada de discagem incremental ou discagem atrasada.

Quando o endereço fornecido estiver incompleto, a discagem de alguns dos dígitos pode ser atrasada colocando-se um ponto-e-vírgula (;) no final do número. Uma operação de discagem é usada para enviar dados de endereço adicionais na sessão existente, como a discagem do endereço de uma entidade para a qual a chamada será transferida.

Cada provedor de serviços deve rejeitar uma cadeia de caracteres de discagem que contém o **?** e deixe o aplicativo lidar com ele conforme apropriado. Por exemplo, o aplicativo poderia usar a discagem parcial para discar a cadeia de caracteres, até, mas não incluindo o **?** e, em seguida, exibir uma caixa de diálogo para permitir que o usuário sinalize quando o restante da cadeia de caracteres de discagem deve ser discado.

Um motivo adicional para um aplicativo usar a discagem parcial é se o provedor de serviços não dá suporte a um ou mais dos caracteres de controle de detecção de andamento da chamada. Esses caracteres, que podem ocorrer em um endereço de discagem, são W (aguardar o tom de discagem); @ (aguardar resposta silenciosa); e $ (aguarde o tom de prompt do cartão de chamada). Esses e todos os outros caracteres usados em cadeias de endereços são discutidos com mais detalhes em [endereços de discagem](address-ovr.md).

O provedor indica a quais modificadores de cadeia de caracteres de discagem "aguardar" são compatíveis. Um aplicativo TAPI 2 encontra esses dados no membro **dwDevCapFlags** da estrutura [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) retornada pelo [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps). Um aplicativo TAPI 3 chama [**ITAddressCapabilities:: get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) com *AddressCap* definido como o membro **CA \_ DEVCAPFLAGS** do [**\_ recurso de endereço**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).

O aplicativo pode optar por examinar as cadeias de caracteres de discagem para um caractere sem suporte ou pode passar a cadeia de caracteres "RAW" como parte da inicialização de uma sessão. Se a cadeia de caracteres contiver um modificador sem suporte ou um "?", o provedor retornará um erro indicando qual modificador incorreto ocorreu primeiro na cadeia de caracteres:

-   LINEERR \_ DIALBILLING
-   LINEERR \_ DIALQUIET
-   LINEERR \_ DIALDIALTONE
-   LINEERR \_ DIALPROMPT

Em seguida, o aplicativo pode localizar o modificador incorreto na cadeia de caracteres, pegar os dígitos à esquerda do modificador, acrescentar um ponto e vírgula e iniciar uma sessão usando o endereço parcial. O restante da cadeia de caracteres pode ser enviado usando a operação de discagem.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial).

**TAPI 3. x:** Consulte [**ITBasicCallControl::D Ste**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial).

 

 
