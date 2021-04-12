---
title: Subentradas e conexões Multilink
description: O Windows NT Server 4,0 fornece suporte para subentradas de catálogo telefônico, que habilitam conexões de Multilink. Uma conexão Multilink combina a largura de banda de várias conexões para fornecer uma única conexão com maior largura de banda.
ms.assetid: 19cf6e1a-cdba-47e4-8d8f-d6030ed6f9e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1970e2e2ad668b376b1097aa20cd18986fb605a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294374"
---
# <a name="subentries-and-multilink-connections"></a>Subentradas e conexões Multilink

O Windows NT Server 4,0 fornece suporte para subentradas de catálogo telefônico, que habilitam conexões de Multilink. Uma conexão Multilink combina a largura de banda de várias conexões para fornecer uma única conexão com maior largura de banda.

Uma entrada do catálogo telefônico RAS pode ter zero ou mais subentradas. A função [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) recupera uma estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) que inclui informações sobre as subentradas de uma entrada de catálogo telefônico. O membro **dwSubEntries** da estrutura **RASENTRY** indica o número de subentradas. As entradas do catálogo telefônico inicialmente não têm subentradas. Para adicionar subentradas a uma entrada de catálogo telefônico, use a função [**RasSetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa) .

As propriedades de cada subentrada incluem um número de telefone e o nome e o tipo do dispositivo TAPI a ser usado ao discar a subentrada. Além disso, uma subentrada pode incluir uma lista de números de telefone alternativos a serem discados se o RAS não puder estabelecer uma conexão usando o número primário. As funções [**RasSetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa) e [**RasGetSubEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetsubentrypropertiesa) usam a estrutura [**RASSUBENTRY**](/previous-versions/windows/desktop/legacy/aa377839(v=vs.85)) para definir e recuperar as propriedades de uma subentrada de catálogo telefônico especificada. As subentradas são identificadas por um índice baseado em um.

Você pode chamar a função [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para configurar uma entrada de Ras de múltiplos vínculos para conectar todas as subentradas quando ele for discado pela primeira vez. Como alternativa, você pode configurar uma entrada para fornecer largura de banda variável. Nesse caso, o RAS conecta uma única subentrada inicialmente e, em seguida, conecta ou desconecta outras subscrições conforme necessário. Para uma conexão Multilink de largura de banda variável, você pode usar a estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) para especificar a subentrada inicial a ser conectada ao chamar a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Ao usar a função [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) para conectar uma entrada de multilink, você pode usar a estrutura [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) para especificar a subentrada inicial a ser conectada.

Para uma conexão Multilink de largura de banda variável, use a estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) com a função [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para especificar os parâmetros para conectar e desconectar as subentradas individuais. O RAS conecta uma subentrada adicional quando a largura de banda que está sendo usada excede um percentual especificado da largura de banda disponível para um intervalo especificado.

Se você chamar a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para estabelecer uma conexão de vínculos múltiplos, poderá especificar uma função de retorno de chamada [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) para receber notificações sobre a conexão. **RasDialFunc2** é semelhante à função de retorno de chamada [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) , exceto pelo fato de que ela fornece informações adicionais para uma conexão Multilink, como o índice da subentrada que causou a notificação. O RAS chama sua função **RasDialFunc2** quando conecta ou desconecta uma subentrada.

Você pode usar um identificador de conexão **HRASCONN** para desligar ou recuperar informações sobre uma conexão de vínculos múltiplos. Você pode obter um identificador de conexão para cada uma das conexões de subentrada que compõem o Multilink, bem como para a conexão de multilink combinada. Quando você chama a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para estabelecer uma conexão de vínculos múltiplos, **RasDial** retorna um identificador para a conexão de multilink combinada. Da mesma forma, [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) retorna o identificador de multilink combinado quando você enumera conexões. Para obter um identificador para uma das conexões de subentrada em uma conexão de vínculos múltiplos, chame a função [**RasGetSubEntryHandle**](/windows/desktop/api/Ras/nf-ras-rasgetsubentryhandlea) .

Você pode usar o identificador de conexão Multilink combinado e os identificadores de conexão de subentrada nas funções [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa), [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)e [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) . Chamar **RasHangUp** com um identificador de multilink combinado encerra toda a conexão; chamá-lo com um identificador de subentrada desliga apenas essa conexão de subentrada. Da mesma forma, **RasGetConnectStatus** retorna informações para a conexão combinada ou individual, dependendo do identificador especificado. As informações de projeção retornadas por **RasGetProjectionInfo** para uma entrada de multilink são as mesmas para cada um dos identificadores de conexão de subentrada como é para o identificador de conexão principal.

 

 