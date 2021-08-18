---
description: As funções a seguir são usadas com os recursos de comunicação.
ms.assetid: ba7d1a9e-6906-4923-a8eb-db58050ba699
title: Funções de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1f49efccf2ff93ea18710ea4d6647e45f1135cf8a5fed542a65192f0abda6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768956"
---
# <a name="communications-functions"></a>Funções de comunicação

As funções a seguir são usadas com os recursos de comunicação.



| Função                                                   | Descrição                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)                       | Preenche uma estrutura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) especificada com valores especificados em uma cadeia de caracteres de controle de dispositivo.                           |
| [**BuildCommDCBAndTimeouts**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcbandtimeoutsa) | Converte uma cadeia de caracteres de definição de dispositivo em códigos de bloco de controle de dispositivo apropriados e os coloca em um bloco de controle de dispositivo. |
| [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak)                   | Restaura a transmissão de caracteres para um dispositivo de comunicações especificado e coloca a linha de transmissão em um estado nonbreak.    |
| [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror)                   | Recupera informações sobre um erro de comunicação e relata o status atual de um dispositivo de comunicações.                  |
| [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga)               | Exibe uma caixa de diálogo de configuração fornecida pelo driver.                                                                           |
| [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction)           | Direciona um dispositivo de comunicações especificado para executar uma função estendida.                                                     |
| [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig)                     | Recupera a configuração atual de um dispositivo de comunicações.                                                                |
| [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask)                         | Recupera o valor da máscara de evento para um dispositivo de comunicações especificado.                                                   |
| [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)           | Recupera os valores de registro de controle de modem.                                                                                       |
| [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties)             | Recupera informações sobre as propriedades de comunicação de um dispositivo de comunicações especificado.                               |
| [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate)                       | Recupera as configurações de controle atuais para um dispositivo de comunicações especificado.                                                  |
| [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)                 | Recupera os parâmetros de tempo limite para todas as operações de leitura e gravação em um dispositivo de comunicações especificado.                      |
| [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga)       | Recupera a configuração padrão para o dispositivo de comunicações especificado.                                                   |
| [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm)                             | Descarta todos os caracteres da saída ou do buffer de entrada de um recurso de comunicação especificado.                                |
| [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak)                       | Suspende a transmissão de caracteres para um dispositivo de comunicações especificado e coloca a linha de transmissão em um estado de interrupção.       |
| [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig)                     | Define a configuração atual de um dispositivo de comunicações.                                                                     |
| [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)                         | Especifica um conjunto de eventos a ser monitorado para um dispositivo de comunicações.                                                         |
| [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)                       | Configura um dispositivo de comunicações de acordo com as especificações em um bloco de controle de dispositivo.                                  |
| [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)                 | Define os parâmetros de tempo limite para todas as operações de leitura e gravação em um dispositivo de comunicações especificado.                           |
| [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)       | Define a configuração padrão para um dispositivo de comunicações.                                                                    |
| [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)                             | Inicializa os parâmetros de comunicação para um dispositivo de comunicações especificado.                                               |
| [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar)               | Transmite um caractere especificado à frente de todos os dados pendentes no buffer de saída do dispositivo de comunicações especificado.         |
| [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)                     | Aguarda a ocorrência de um evento para um dispositivo de comunicações especificado.                                                             |



 

 

 



