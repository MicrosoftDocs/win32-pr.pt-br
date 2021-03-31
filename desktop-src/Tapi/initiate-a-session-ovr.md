---
description: As informações primárias que um aplicativo fornece para iniciar uma sessão de comunicações são o tipo de endereço, o tipo de mídia ou os tipos e o endereço de destino.
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: Iniciar uma sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e925ba90460b88c85a9aab1624923acdbc4572a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827758"
---
# <a name="initiate-a-session"></a>Iniciar uma sessão

As informações primárias que um aplicativo fornece para iniciar uma sessão de comunicações são o [tipo de endereço](address-type-ovr.md), o tipo de [mídia](media-type-ovr.md) ou os tipos e o [endereço](address-ovr.md)de destino.

O endereço de destino pode exigir a [conversão de endereços](#address-translation) para colocar as informações inseridas por um usuário no formato adequado para um determinado tipo de endereço. Por exemplo, um número de telefone que estava em um catálogo de endereços eletrônicos em formato [canônico](address-ovr.md) exigirá tradução para o formato de [discagem](address-ovr.md) .

Algumas sessões podem exigir parâmetros de configuração especiais, se houver suporte do provedor de serviços. Por exemplo, um ISDN TSP pode transmitir informações do usuário e algumas MSPs exigem informações sobre a direção do fluxo de mídia. Consulte [as informações da sessão](session-information-ovr.md) para obter uma revisão dos dados que podem ser definidos ou obtidos em relação a uma sessão.

Depois que uma sessão for iniciada, a TAPI informará o aplicativo de andamento da chamada usando o mecanismo de notificação de eventos configurado durante a inicialização.

**TAPI 2. x:** Os aplicativos iniciam uma sessão usando a função [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) . A função [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) é usada para executar a conversão de endereço, se necessário.

Parâmetros de configuração de chamada podem ser armazenados na estrutura de dados [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams) e um ponteiro para essa estrutura é usado como um parâmetro de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall). Se nenhuma estrutura **LINECALLPARAMS** for fornecida para **lineMakeCall**, uma chamada de taxa de voz POTS padrão será solicitada com um conjunto de valores padrão.

Se a sessão for configurada com êxito, um identificador de chamada com [privilégios](privilege-ovr.md) de *proprietário* será retornado ao aplicativo e a TAPI enviará as mensagens [**\_ callstate de linha**](./line-callstate.md) de aplicativo com informações relacionadas ao progresso da chamada. Normalmente, os aplicativos usam essas mensagens para exibir relatórios de status para o usuário.

**TAPI 3. x:** Os aplicativos iniciam uma sessão de comunicações invocando o método [**ITAddress:: createcall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) em um endereço capaz de lidar com o tipo de endereço e o tipo de mídia necessários. Se o endereço expõe a interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) , os terminais são selecionados nos fluxos de mídia do objeto de chamada. Consulte o exemplo [criar um](make-a-call.md) código de chamada para obter uma ilustração desse processo.

Parâmetros de configuração de chamada podem ser armazenados ou alterados usando métodos expostos pela interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

Se a sessão for configurada com êxito, a TAPI retornará um ponteiro de interface [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) que pode ser usado para operações de sessão adicionais ou para obter um ponteiro de interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) que possa ser usado para obter informações de sessão adicional. A interface [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) processa eventos de estado de chamada TAPI.

> [!Note]  
> A TAPI não deve ser usada para transmissões de fax. Em vez disso, use as funções disponíveis por MAPI, a API do sistema de mensagens da Microsoft.

 

## <a name="address-translation"></a>Conversão de endereço

Um aplicativo de usuário final ou de servidor pode armazenar endereços em um formato que não é compatível com as necessidades de um determinado provedor de serviços. Por exemplo, um número de telefone pode ser armazenado em um catálogo de endereços eletrônicos em [formato canônico](address-ovr.md), mas a maioria dos provedores de serviços que lidam com números de telefone exigem o [formato de discagem](address-ovr.md).

A TAPI fornece operações de conversão de endereços que auxiliam um aplicativo na apresentação do tipo de endereço correto para um TSP. O provedor de serviços especifica a TAPI a qual tipo de endereço ele dá suporte e não precisa incluir nenhuma forma de conversão de endereço.

**TAPI 2. x:** Consulte [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress).

**TAPI 3:** Consulte [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo).

## <a name="toll-lists"></a>Listas de chamadas

Em alguns locais no América do Norte, todas as chamadas telefônicas colocadas no código de área local são chamadas locais. Em outros locais, algumas chamadas colocadas no código de área local são de longa distância e precisam de um prefixo "1" para serem discados. Os três primeiros dígitos do endereço (o prefixo) determinam se uma chamada no código de área local é uma chamada de chamada.

Uma *lista de chamadas* é uma lista de prefixos no código de área local cujos endereços devem ser discados como endereços de longa distância e são avaliados como encargos de longa distância.

Listas de chamadas não são relevantes para provedores de serviço ou para aplicativos que não acessam uma rede telefônica.

**TAPI 2. x:** Consulte [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) (LINETRANSLATERESULT \_ e LINETRANSLATERESULT \_ NOTINTOLLLIST bits na estrutura [**LINETRANSLATEOUTPUT**](/windows/win32/api/tapi/ns-tapi-linetranslateoutput) ), [**lineSetTollList**](/windows/win32/api/tapi/nf-tapi-linesettolllist).

**TAPI 3:** Consulte [**ITAddressTranslation:: TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress), [**ITAddressTranslationInfo:: get \_ TranslationResults**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults).

 

 
