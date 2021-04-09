---
description: Quando a função CreateFile abre um identificador para um recurso de comunicações serial, o sistema inicializa e configura o recurso de acordo com os valores configurados na última vez em que o recurso foi aberto.
ms.assetid: a39881d8-32af-4846-a2d3-508f1945b666
title: Modificação das configurações de recursos de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8658029470fae9ee2d70ffb1459312c3c4d80ecf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010190"
---
# <a name="modification-of-communications-resource-settings"></a>Modificação das configurações de recursos de comunicação

Quando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) abre um identificador para um recurso de comunicações serial, o sistema inicializa e configura o recurso de acordo com os valores configurados na última vez em que o recurso foi aberto. Preservar as configurações anteriores permite que o usuário retenha as configurações especificadas por meio de um comando de **modo** quando o dispositivo é reaberto. Os valores herdados da operação de abertura anterior incluem as definições de configuração do bloco de controle de dispositivo (uma estrutura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) ) e os valores de tempo limite usados em operações de e/s. Se o dispositivo nunca tiver sido aberto, ele será configurado com os padrões do sistema.

Para determinar a configuração inicial de um recurso de comunicações serial, um processo chama a função [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) , que preenche uma estrutura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) de porta serial com as definições de configuração atuais. Para modificar essa configuração, um processo especifica uma estrutura **DCB** em uma chamada para a função [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) .

Os membros da estrutura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) especificam as definições de configuração, como a taxa de transmissão, o número de bits de dados por byte e o número de bits de parada por byte. Outros membros do **DCB** especificam caracteres especiais e habilitam a verificação de paridade e o controle de fluxo. Quando um processo precisa modificar apenas algumas dessas definições de configuração, ele deve primeiro chamar [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) para preencher uma estrutura **DCB** com a configuração atual. Em seguida, o processo pode ajustar os valores importantes na estrutura **DCB** e reconfigurar o dispositivo chamando [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) e especificando a estrutura **DCB** modificada. Esse procedimento garante que os membros não modificados da estrutura **DCB** contenham valores apropriados. Por exemplo, um erro comum é configurar um dispositivo com uma estrutura **DCB** na qual o membro **XonChar** da estrutura seja igual ao membro **XoffChar** .

A função [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba) fornece outra maneira de modificar uma estrutura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) . **BuildCommDCB** usa uma cadeia de caracteres com a mesma forma que os argumentos de linha de comando do comando **Mode** para especificar a taxa de transmissão, o esquema de paridade, o número de bits de parada e o número de bits de dados. Os membros restantes de [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) não são alterados por essa função, exceto que os membros apropriados são definidos para desabilitar o controle de fluxo de hardware e XON/XOFF. **BuildCommDCB** modifica apenas uma estrutura **DCB** ; Ele não reconfigura o dispositivo.

Um processo pode reconfigurar um recurso de comunicação usando a função [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) para obter informações de um driver de dispositivo sobre as definições de configuração que ele suporta. O processo pode usar essas informações para evitar a especificação de uma configuração sem suporte.

A função [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) reconfigura o recurso de comunicação, mas não afeta os buffers de entrada e saída internos do driver especificado. Os buffers não são liberados e as operações de leitura e gravação pendentes não são encerradas prematuramente.

Um processo reinicializa um recurso de comunicação usando a função [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm) , que executa as seguintes tarefas:

-   Encerra as operações de leitura e gravação pendentes, mesmo que elas não tenham sido concluídas.
-   Descarta caracteres não lidos e libera os buffers de entrada e saída internos do driver associado ao recurso especificado.
-   Realoca os buffers de entrada e saída internos.

Um processo não é necessário para chamar [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm). Caso contrário, o driver do recurso Inicializa o dispositivo com as configurações padrão na primeira vez que o identificador de recursos de comunicação é usado.

 

 
