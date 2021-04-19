---
description: Esta seção contém uma lista das mensagens na interface do provedor de serviços de telefonia (TSPI).
ms.assetid: 3d8bf980-81d6-49db-954f-af72458365dc
title: Mensagens TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5772a1ccb0c07f03b2a17348ecf5e4834bb97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779440"
---
# <a name="tspi-messages"></a>Mensagens TSPI

Esta seção contém uma lista das mensagens na interface do provedor de serviços de telefonia (TSPI). Essas mensagens são usadas para notificar a TAPI sobre a ocorrência de eventos assíncronos que ocorrem espontaneamente dentro do provedor de serviços. O provedor de serviços passa esses eventos para a TAPI chamando uma função de retorno de chamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) ou [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) , dependendo se o provedor de serviços está relatando um evento em um dispositivo de linha, chamada ou telefone. O procedimento **LINEEVENT** para relatar eventos que ocorrem em uma linha ou chamada é fornecido ao provedor de serviços no momento em que a linha é aberta com a função [**\_ lineOpen do TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) . O procedimento **PHONEEVENT** para relatar eventos que ocorrem em um telefone é fornecido com a [**função \_ phoneOpen do TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen) .

Esses eventos ESPONTANEOS não são solicitados pela TAPI, no sentido de que eles não são uma resposta direta a qualquer solicitação. Esses eventos contrastam com a conclusão dos relatórios de solicitações feitas pela TAPI. Esses eventos de conclusão são relatados pela função de retorno de chamada de [**\_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Os perfis de parâmetro dos procedimentos de evento espontaneal incluem parâmetros que identificam o objeto relevante para o qual o evento está sendo relatado (telefone, linha ou chamada). A identificação está na forma de um identificador opaco cuja interpretação exata não é publicada pelo TSPI. A TAPI internamente determina a relação entre esses identificadores opacos e quaisquer estruturas de dados usadas para representar os dispositivos.

O perfil de parâmetro para procedimentos de evento de espontaneidade também inclui um parâmetro de mensagem que identifica o tipo da mensagem. Cada tipo de mensagem tem uma definição correspondente que determina os identificadores que são incluídos, juntamente com outros parâmetros e seus significados. Há uma correspondência muito forte entre as mensagens que aparecem no nível de TSPI e as que aparecem no nível da TAPI. Estas são as regras gerais de correspondência:

-   O conjunto de mensagens é quase idêntico. Quando as mensagens correspondem, o mesmo nome de mensagem e valor são usados no nível de TSPI.
-   Os identificadores que aparecem no nível de TSPI são os tipos opacos definidos pela especificação TSPI. Esses tipos (e sua interpretação) diferem daqueles no nível da TAPI, embora eles se refiram à mesma classe de dispositivo. Por exemplo, em que uma mensagem TAPI inclui um identificador HLINE, a mensagem TSPI correspondente normalmente incluiria um identificador [**HTAPILINE**](htapiline.md) .
-   Não há dados de *dwCallBackInstance* passados para o retorno de chamada.
-   Os parâmetros *dwParam1*, *dwParam2* e *dwParam3* são geralmente idênticos aos parâmetros correspondentes para a mensagem TAPI.
-   As mensagens orientadas a linha e orientadas a chamadas são passadas para um procedimento de retorno de chamada diferente de mensagens orientadas por telefone.

Para cada mensagem, esta seção lista os seguintes itens:

-   A finalidade da mensagem
-   O procedimento de retorno de chamada para o qual esta mensagem é passada
-   Uma descrição dos parâmetros da mensagem
-   Comentários opcionais sobre como usar a mensagem
-   Referências opcionais a outras funções, mensagens e estruturas de dados
-   Comentários opcionais comparando esta mensagem à interface TAPI

Determinadas mensagens são usadas para notificar a TAPI sobre uma alteração no status de um objeto. Essas mensagens fornecem o identificador de objeto TAPI opaco e uma indicação de qual item de status foi alterado. A TAPI pode, subsequentemente, chamar uma função apropriada de "Get status" do objeto para obter o status completo do objeto.

Quando ocorre um evento, uma mensagem pode ou não ser enviada para a TAPI. Para alguns tipos de eventos, como alterações de status, a TAPI especifica um conjunto de alterações de status em que ele está interessado. O provedor de serviços é aconselhado a limitar os eventos de mensagem de alteração de status que ele relata para aqueles incluídos neste conjunto. O provedor de serviços não precisa aderir a esse limite. Em outras palavras, ele pode relatar mais alterações do que são estritamente necessárias. No entanto, ele deve tentar observar o limite por motivos de desempenho.

A mensagem de resposta de linha \_ não é usada no nível de TSPI. A conclusão de uma solicitação assíncrona é relatada usando o retorno de chamada de [**\_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) .

A mensagem de resposta do telefone \_ não é usada no nível de TSPI. A conclusão de uma solicitação assíncrona é relatada usando o retorno de chamada de [**\_ conclusão assíncrona**](/windows/win32/api/tspi/nc-tspi-async_completion) .

Para obter mais informações, consulte estes tópicos:

-   [Mensagens do dispositivo TSPI line](tspi-line-device-messages.md)
-   [Mensagens do dispositivo TSPI Phone](tspi-phone-device-messages.md)

 

 
