---
description: Um identificador para um recurso de comunicação tem um conjunto associado de parâmetros de tempo limite que afetam o comportamento de operações de leitura e gravação.
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: Intervalos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6226e8a2d13020bd4dc90a416e7ef359fbd919cf54e886c5e691e5fca2cdea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956785"
---
# <a name="time-outs"></a>Intervalos

Um identificador para um recurso de comunicação tem um conjunto associado de parâmetros de tempo limite que afetam o comportamento de operações de leitura e gravação. Os tempos limite podem fazer com que uma operação [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)ou [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) seja concluída quando um intervalo de tempo limite expirar, embora o número especificado de caracteres não tenha sido lido ou gravado. Ele não é tratado como um erro quando um tempo limite ocorre durante uma operação de leitura ou gravação (ou seja, o valor de retorno da função de leitura ou gravação indica êxito). A contagem de bytes realmente lidos ou gravados é relatada por **ReadFile** ou **WriteFile** (ou pela função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) ou [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) , se a e/s foi executada como uma operação sobreposta).

Quando um aplicativo abre um recurso de comunicação, o sistema define os valores de tempo limite do recurso para os valores em vigor quando o recurso foi usado pela última vez. Se o recurso de comunicação nunca tiver sido aberto, o sistema definirá os valores de tempo limite como um valor padrão. Em ambos os casos, um aplicativo sempre deve determinar os valores de tempo limite atuais depois de abrir o recurso e, em seguida, defini-los explicitamente para atender aos seus requisitos. Para determinar os valores de tempo limite atuais de um recurso de comunicação, use a função [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) . Para alterar os valores de tempo limite, use a função [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) .

Dois tipos de tempo limite são habilitados pelos parâmetros de tempo limite. Um tempo limite de intervalo ocorre quando o tempo entre o recebimento de dois caracteres excede um número especificado de milissegundos. O tempo começa quando o primeiro caractere é recebido e é reiniciado quando cada caractere novo é recebido. Um tempo limite total ocorre quando a quantidade total de tempo consumido por uma operação de leitura excede um número calculado de milissegundos. O tempo começa imediatamente quando a operação de e/s é iniciada. As operações de gravação dão suporte apenas ao tempo limite total. As operações de leitura dão suporte a intervalo e tempos limite totais, que podem ser usados separadamente ou combinados.

O tempo, em milissegundos, do período de tempo limite total para uma operação de leitura ou gravação é calculado usando os valores de valor de multiplicador e constante da estrutura [**COMMTIMEOUTS**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts) especificada na função [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) ou [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) . A fórmula a seguir é usada:


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



Usar um multiplicador e uma constante permite que o período de tempo limite total varie, dependendo da quantidade de dados que estão sendo solicitados. Um aplicativo pode usar apenas a constante definindo o multiplicador como zero ou usar apenas o multiplicador definindo a constante como zero. Se a constante e o multiplicador forem zero, o tempo limite total não será usado.

Se todos os parâmetros de tempo limite de leitura forem zero, os tempos limite de leitura não serão usados e uma operação de leitura não será concluída até que o número solicitado de bytes tenha sido lido ou um erro ocorra. Da mesma forma, se todos os parâmetros de tempo limite de gravação forem zero, uma operação de gravação não será concluída até que o número solicitado de bytes tenha sido gravado ou um erro ocorra.

Se o parâmetro de tempo limite do intervalo de leitura for o valor **MAXDWORD** e os parâmetros de tempo limite total de leitura forem zero, uma operação de leitura será concluída imediatamente após a leitura de quaisquer caracteres disponíveis no buffer de entrada, mesmo se ele estiver vazio.

O tempo de intervalo força uma operação de leitura a retornar quando há um pausa na recepção. Um processo que usa tempos limite de intervalo pode definir um parâmetro de intervalo razoavelmente curto, para que ele possa responder rapidamente a pequenas intermitências isoladas de um ou alguns caracteres, ainda que ainda possa coletar grandes buffers de caracteres com uma única chamada quando os dados forem recebidos em um fluxo constante.

Os tempos limite para uma operação de gravação podem ser úteis quando a transmissão é bloqueada por algum tipo de controle de fluxo ou quando a função [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) foi chamada para suspender a transmissão de caracteres.

A tabela a seguir resume o comportamento das operações de leitura com base nos valores especificados para tempos limite de totais e intervalos.



| Total | Intervalo | Comportamento                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | Retorna quando o buffer é completamente preenchido. Os tempos limite não são usados.                                                                                                                    |
| T     | 0        | Retorna quando o buffer é completamente preenchido ou quando T milissegundos decorrem desde o início da operação.                                                                   |
| 0     | Y        | Retorna quando o buffer é completamente preenchido ou quando Y milissegundos decorreu entre o recebimento de dois caracteres. O tempo não começa até que o primeiro caractere seja recebido. |
| T     | Y        | Retorna quando o buffer é completamente preenchido ou quando um dos tipos de tempo limite ocorre.                                                                                                     |



 

> [!Note]  
> No entanto, esse intervalo é relativo ao sistema que controla o dispositivo físico. Para um dispositivo remoto, como um modem, o tempo é relativo ao sistema de servidor ao qual o modem está anexado. Qualquer atraso de propagação de rede não é fatorado no. Por exemplo, um aplicativo cliente pode especificar um tempo limite total que computa para 500 milissegundos. Quando 500 milissegundos tiverem decorrido no servidor, um erro de tempo limite será retornado ao cliente. Se houver um atraso de propagação de rede de 50 milissegundos, o cliente não será notificado sobre o tempo limite até aproximadamente 50 milissegundos depois que o tempo limite realmente ocorrer.

 

> [!Note]  
> Os parâmetros de tempo limite afetam o comportamento das operações de leitura e gravação sobrepostas em um dispositivo de comunicações. Com e/s sobreposta, a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)ou [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) pode retornar antes que a operação seja concluída. Os parâmetros de tempo limite podem determinar quando a operação foi concluída.

 

 

 
