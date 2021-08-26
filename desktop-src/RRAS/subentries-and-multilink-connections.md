---
title: Sub-entradas e conexões multilink
description: Windows NT O Servidor 4.0 dá suporte a sub-entradas de lista telefônica, que habilitam conexões multilink. Uma conexão multilink combina a largura de banda de várias conexões para fornecer uma única conexão com maior largura de banda.
ms.assetid: 19cf6e1a-cdba-47e4-8d8f-d6030ed6f9e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cdada1e48ffc42753480a6a62fb79986d537402ad21449617359cd49df76f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101796"
---
# <a name="subentries-and-multilink-connections"></a>Sub-entradas e conexões multilink

Windows NT O Servidor 4.0 dá suporte a sub-entradas de lista telefônica, que habilitam conexões multilink. Uma conexão multilink combina a largura de banda de várias conexões para fornecer uma única conexão com maior largura de banda.

Uma entrada de livro telefônica RAS pode ter zero ou mais subentradas. A [**função RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) recupera uma estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) que inclui informações sobre as subentradas de uma entrada de livro de telefone. O **membro dwSubEntries** da **estrutura RASENTRY** indica o número de subentradas. Telefone de livro não têm nenhuma sub-entrada inicialmente. Para adicionar subentradas a uma entrada de phone-book, use a [**função RasSetSubEntryProperties.**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa)

As propriedades de cada subentrada incluem um número de telefone e o nome e o tipo do dispositivo TAPI a ser usado ao discar a subentrada. Além disso, uma subentrada pode incluir uma lista de números de telefone alternativos para discar se o RAS não puder fazer uma conexão usando o número primário. As [**funções RasSetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa) e [**RasGetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetsubentrypropertiesa) usam a estrutura [**RASSUBENTRY**](/previous-versions/windows/desktop/legacy/aa377839(v=vs.85)) para definir e recuperar as propriedades de uma subentrada de phone-book especificada. As sub-entradas são identificadas por um índice baseado em um.

Você pode chamar a [**função RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para configurar uma entrada RAS multilink para conectar todas as subentradas quando ela for discada pela primeira vez. Como alternativa, você pode configurar uma entrada para fornecer largura de banda variável. Nesse caso, o RAS conecta uma única subentrada inicialmente e, em seguida, conecta ou desconecta subentradas adicionais conforme necessário. Para uma conexão multilink de largura de banda variável, você pode usar a estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) para especificar a subentrada inicial para se conectar ao chamar a [**função RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Ao usar a [**função RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) para conectar uma entrada multilink, você pode usar a estrutura [**RASDIALDLG**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) para especificar a subentrada inicial para se conectar.

Para uma conexão multilink de largura de banda variável, use a estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) com a [**função RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para especificar os parâmetros para conectar e desconectar as subentradas individuais. O RAS conecta uma subentrada adicional quando a largura de banda que está sendo usada excede um percentual especificado da largura de banda disponível para um intervalo especificado.

Se você chamar a [**função RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para estabelecer uma conexão multilink, poderá especificar uma função de retorno de chamada [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) para receber notificações sobre a conexão. **RasDialFunc2** é semelhante à função de retorno de chamada [**RasDialFunc1,**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) exceto pelo fato de que ele fornece informações adicionais para uma conexão multilink, como o índice da subentrada que causou a notificação. RAS chama sua **função RasDialFunc2** quando ela se conecta ou desconecta uma subentrada.

Você pode usar um alça **de conexão HRASCONN** para desligar ou recuperar informações sobre uma conexão multilink. Você pode obter um alça de conexão para cada uma das conexões de subentrada que comem o multilink, bem como para a conexão multilink combinada. Quando você chama a [**função RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para estabelecer uma conexão multilink, **RasDial** retorna um handle para a conexão multilink combinada. Da mesma forma, [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) retorna o handle multilink combinado quando você enumera conexões. Para obter um handle para uma das conexões de subentrada em uma conexão multilink, chame a [**função RasGetSubEntryHandle.**](/windows/desktop/api/Ras/nf-ras-rasgetsubentryhandlea)

Você pode usar o alça de conexão multilink combinado e os alças de conexão de subentrada nas funções [**RasGetUp,**](/windows/desktop/api/Ras/nf-ras-rashangupa) [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)e [**RasGetProjectionInfo.**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) Chamar **RasLinkUp** com um handle multilink combinado encerra toda a conexão; chamá-lo com um alça de subentrada trava apenas essa conexão de subentrada. Da mesma forma, **RasGetConnectStatus retorna** informações para a conexão combinada ou individual, dependendo do handle especificado. As informações de projeção retornadas por **RasGetProjectionInfo** para uma entrada multilink são as mesmas para cada um dos alças de conexão de subentrada como são para o alçamento de conexão principal.

 

 