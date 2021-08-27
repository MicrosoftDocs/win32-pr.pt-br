---
description: Quando um opertion retorna êxito, a função progrediu com êxito para um ponto que é definido pela API em uma base de função por função.
ms.assetid: e4077d77-dee1-4f1a-a6ee-20ca2f92a1ec
title: O significado do sucesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae38aa834b3c60107c0245be2c792703a9c038c6e9b96f982e720bf417af58f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126116"
---
# <a name="the-meaning-of-success"></a>O significado do sucesso

## <a name="tapi-2x"></a>TAPI 2. x

Quando uma operação retorna uma indicação de êxito (de forma síncrona após o retorno da função para operações síncronas, ou assincronamente por meio de uma [**\_ resposta de linha**](./line-reply.md) ou mensagem de [**\_ resposta de telefone**](./phone-reply.md) para operações assíncronas), presume-se que o seguinte seja verdadeiro:

-   A função progrediu com êxito para um ponto definido pela API em uma base função a função. Depois que esse ponto tiver sido atingido, a operação será completamente concluída ou estará em um estado, de modo que as mensagens de estado independentes informarão o aplicativo sobre o progresso subsequente.

    Por exemplo, a implementação de um provedor de serviço de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) deve retornar Success não mais tarde quando a chamada entrar no estado de chamada de continuação. O ideal é que o provedor indique sucesso assim que possível, como quando a chamada entra no estado de chamada de sinal de discagem (se aplicável). Depois que o sucesso for retornado para o aplicativo, \_ as mensagens callstate de linha informarão o aplicativo sobre o progresso da chamada. Provedores de serviço que atrasam o retorno da indicação de êxito **lineMakeCall** , por exemplo, até que a discagem seja concluída, deve estar ciente de que isso coloca esse provedor em uma desvantagem, pois a usabilidade no nível do aplicativo pode ser severamente limitada. Por exemplo, não seria possível que um usuário cancele a solicitação de configuração de chamada em andamento até que a discagem seja concluída e todos os dígitos tenham sido enviados para o comutador.

-   As funções que retornam informações (como [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)) retornam êxito somente quando as informações solicitadas estão disponíveis para o aplicativo. As funções que retornam identificadores (para linhas ou chamadas) podem retornar êxito somente depois que o identificador for válido. Nenhuma mensagem deve ser enviada sobre essa linha ou chamada antes da indicação de êxito da função que causou a criação. O provedor de serviços é responsável por suprimir essas mensagens.
-   As funções que habilitam determinadas condições permanentes (como [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)) retornam êxito somente após a condição ser habilitada, não quando a condição for removida novamente (por exemplo, não quando todo o monitoramento de dígitos for concluído).
-   As funções de controle de chamada (como [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold) ou [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), mas não [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall)) retornam êxito quando a operação é concluída. Algumas redes telefônicas não fornecem confirmação (positiva ou negativa) sobre a conclusão de determinadas solicitações feitas pelos provedores de serviços. Nessas situações, o provedor de serviços deve decidir sobre êxito ou falha da solicitação. Portanto, o sucesso pode indicar que o provedor de serviços iniciou ações para atender à solicitação, mas não necessariamente mais nada. Por exemplo, o provedor pode não receber nenhuma confirmação de afirmativo para sua solicitação do comutador, embora já tenha enviado uma mensagem de êxito ao aplicativo.

## <a name="tapi-3x"></a>TAPI 3. x

Quando uma operação retorna uma indicação de êxito (de forma síncrona após o retorno da função para operações síncronas, ou assincronamente com uma chamada para o procedimento de retorno de chamada assíncrono de operações assíncronas), presume-se que o seguinte seja verdadeiro: [**\_**](/windows/win32/api/tspi/nc-tspi-async_completion)

-   A função progrediu com êxito para um ponto definido pelo provedor de serviços. O provedor de serviços define o ponto em uma base função a função. Depois de atingir esse ponto, a operação é completamente concluída ou está em um estado de que as mensagens de estado independentes subsequentes informarão o aplicativo sobre o progresso.
-   As funções que retornam informações (como [**TSPI \_ LinePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark) ou [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)) retornam êxito somente quando as informações solicitadas estão disponíveis para o chamador. As funções que retornam identificadores (para linhas abertas, telefones abertos ou chamadas) retornam os identificadores imediatamente no retorno da função. O provedor de serviços e o chamador devem tratar os identificadores como "ainda não válidos" até a indicação eventual de sucesso. O provedor de serviços é responsável por impedir qualquer mensagem de retorno de chamada para o procedimento [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) ou [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) sobre essa linha aberta, abrir o telefone ou chamar até após a indicação de êxito. Se o resultado eventual for um erro, qualquer identificador retornado imediatamente se tornará inválido sem nenhuma ação adicional.
-   As funções que habilitam determinadas condições permanentes (como [**TSPI \_ lineMonitorDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)) retornam êxito somente após a condição ser habilitada, não quando a condição é removida novamente (por exemplo, não quando o monitoramento de dígitos é concluído).
-   As funções de controle de chamada (como [**TSPI \_ LineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold) e [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer), mas não [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)) retornam êxito quando a operação é concluída. Em ambientes de telefonia que não fornecem uma confirmação positiva dessas funções, o provedor de serviços é forçado a tomar uma decisão de melhor esforço quanto ao sucesso ou à falha da função.
-   A implementação de um provedor de serviços de [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) deve retornar êxito não depois de quando a chamada entrar no estado de chamada em *andamento* . O ideal é que o provedor indique sucesso assim que possível, por exemplo, quando a chamada entra no estado de chamada de *sinal* de discagem (se aplicável). Quando êxito é retornado para o aplicativo, as mensagens [**\_ callstate de linha**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) informam o chamador sobre o progresso da chamada. Os provedores de serviço que atrasam retornam a indicação de sucesso **TSPI \_ lineMakeCall** , por exemplo, até que a discagem seja concluída, severamente limite a flexibilidade no nível do aplicativo. Atraso no retorno de sucesso em **TSPI \_ lineMakeCall** impede que um usuário cancele a solicitação de configuração de chamada em andamento até que a discagem seja concluída e todos os dígitos sejam enviados para a opção.

 

 
