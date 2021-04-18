---
description: 'Há dois tipos de sincronização de e/s (entrada/saída): e/s síncrona e e/SS assíncrona. E/s assíncrona também é conhecida como e/s sobreposta.'
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: E/s síncrona e síncrona
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 071dd2943537dcb6aff67a95cb5e2c3d514f4c1a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105758039"
---
# <a name="synchronous-and-asynchronous-io"></a>E/s síncrona e síncrona

Consulte também [aplicativos de exemplo relacionados a e/s](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io).

Há dois tipos de sincronização de e/s (entrada/saída): e/s síncrona e e/SS assíncrona. E/s assíncrona também é conhecida como e/s sobreposta.

Em *e/s de arquivo síncrono*, um thread inicia uma operação de e/s e entra imediatamente em um estado de espera até que a solicitação de e/s seja concluída. Um thread que executa a e */s de arquivo assíncrono* envia uma solicitação de e/s para o kernel chamando uma função apropriada. Se a solicitação for aceita pelo kernel, o thread de chamada continuará processando outro trabalho até que o kernel sinalize ao thread de que a operação de e/s está concluída. Em seguida, ele interrompe seu trabalho atual e processa os dados da operação de e/s conforme necessário.

Os dois tipos de sincronização são ilustrados na figura a seguir.

![e/s síncrona e síncrona](images/fig2bedit.png)

Em situações em que espera-se que uma solicitação de e/s demore muito tempo, como uma atualização ou um backup de um banco de dados grande ou um link de comunicação lento, a e/s assíncrona geralmente é uma boa maneira de otimizar a eficiência do processamento. No entanto, para operações de e/s relativamente rápidas, a sobrecarga de processamento de solicitações de e/s de kernel e sinais de kernel pode tornar a e/s assíncrona menos benéfica, especialmente se muitas operações de e/s rápidas precisarem ser feitas. Nesse caso, a e/s síncrona seria melhor. Os mecanismos e os detalhes de implementação de como realizar essas tarefas variam de acordo com o tipo de identificador de dispositivo usado e as necessidades específicas do aplicativo. Em outras palavras, geralmente há várias maneiras de resolver o problema.

## <a name="synchronous-and-asynchronous-io-considerations"></a>Considerações de e/s síncronas e assíncronas

Se um arquivo ou dispositivo for aberto para e/s síncrona (ou seja, **o \_ sinalizador \_ de arquivo sobreposto** não for especificado), as chamadas subsequentes para funções como [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) poderão bloquear a execução do thread de chamada até que ocorra um dos seguintes eventos:

-   A operação de e/s é concluída (neste exemplo, uma gravação de dados).
-   Ocorre um erro de E/S. (Por exemplo, o pipe é fechado da outra extremidade.)
-   Foi feito um erro na chamada em si (por exemplo, um ou mais parâmetros não são válidos).
-   Outro thread no processo chama a função [**CancelSynchronousIo**](cancelsynchronousio-func.md) usando o identificador de thread do thread bloqueado, que encerra a e/s para esse thread, falha na operação de e/s.
-   O thread bloqueado é encerrado pelo sistema; por exemplo, o próprio processo é encerrado ou outro thread chama a função [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) usando o identificador do thread bloqueado. (Isso geralmente é considerado um último recurso e não um bom design de aplicativo.)

Em alguns casos, esse atraso pode ser inaceitável para o design e a finalidade do aplicativo, portanto, os designers de aplicativos devem considerar O uso de e/s assíncrona com objetos de sincronização de thread apropriados, como [portas de conclusão de e/s](i-o-completion-ports.md). Para obter mais informações sobre a sincronização de threads, consulte [sobre a sincronização](/windows/desktop/Sync/about-synchronization).

Um processo abre um arquivo para e/s assíncrona em sua chamada para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) especificando o sinalizador de **\_ sinalizador \_ sobreposto do arquivo** no parâmetro *dwFlagsAndAttributes* . Se **o \_ sinalizador \_ de arquivo sobreposto** não for especificado, o arquivo será aberto para e/s síncrona. Quando o arquivo foi aberto para e/s assíncrona, um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) é passado para a chamada para [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Ao executar e/s síncrona, essa estrutura não é necessária em chamadas para **ReadFile** e **WriteFile**.

> [!Note]  
> Se um arquivo ou dispositivo for aberto para e/s assíncrona, as chamadas subsequentes para funções como [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) usando esse identificador geralmente retornarão imediatamente, mas também podem se comportar de forma síncrona em relação à execução bloqueada. Para obter mais informações, confira [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932).

 

Embora [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) seja a função mais comum a ser usada para abrir arquivos, volumes de disco, Pipes anônimos e outros dispositivos semelhantes, as operações de e/s também podem ser executadas usando um identificador *conversão* de outros objetos do sistema, como um soquete criado pelo [**soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket) ou [**aceitam**](/windows/desktop/api/winsock2/nf-winsock2-accept) funções.

Identificadores para objetos de diretório são obtidos chamando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o atributo **arquivo de \_ \_ \_ semântica de backup de sinalizador** . Identificadores de diretório quase nunca são usados — aplicativos de backup são um dos poucos aplicativos que normalmente os usarão.

Depois de abrir o objeto de arquivo para e/s assíncrona, uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) deve ser criada, inicializada e passada corretamente em cada chamada para funções como [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Tenha em mente o seguinte ao usar a estrutura [**sobreposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) em operações assíncronas de leitura e gravação:

-   Não desaloque ou modifique a estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ou o buffer de dados até que todas as operações de e/s assíncronas para o objeto de arquivo tenham sido concluídas.
-   Se você declarar o ponteiro para a estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) como uma variável local, não saia da função local até que todas as operações de e/s assíncronas para o objeto de arquivo tenham sido concluídas. Se a função local for encerrada prematuramente, a estrutura **sobreposta** sairá do escopo e será inacessível para as funções [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) ou [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) que encontrar fora dessa função.

Você também pode criar um evento e colocar o identificador na estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ; as [funções Wait](/windows/desktop/Sync/wait-functions) podem então ser usadas para aguardar a conclusão da operação de e/s aguardando o identificador de evento.

Como mencionado anteriormente, ao trabalhar com um identificador assíncrono, os aplicativos devem tomar cuidado ao fazer determinações sobre quando liberar recursos associados a uma operação de e/s especificada nesse identificador. Se o identificador for desalocado prematuramente, [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) ou [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) poderá relatar incorretamente que a operação de e/s está concluída. Além disso, a função **WriteFile** às vezes retorna **true** com um valor [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) de **\_ êxito de erro**, mesmo que esteja usando um identificador assíncrono (que também pode retornar **false** com **erro \_ e/s \_ pendente**). Os programadores acostumados ao design de e/s síncrono normalmente lançarão os recursos de buffer de dados neste ponto, porque **verdadeiro** e o **\_ êxito do erro** significam que a operação foi concluída. No entanto, se [as portas de conclusão de e/s](i-o-completion-ports.md) estiverem sendo usadas com esse identificador assíncrono, um pacote de conclusão também será enviado, mesmo que a operação de e/s seja concluída imediatamente. Em outras palavras, se o aplicativo liberar recursos após **WriteFile** retornar **true** com o **\_ êxito de erro** além da rotina de porta de conclusão de e/s, ele terá uma condição de erro livre. Neste exemplo, a recomendação seria permitir que a rotina de porta de conclusão seja exclusivamente responsável por todas as operações de liberação para tais recursos.

O sistema não mantém o ponteiro do arquivo em identificadores assíncronos para arquivos e dispositivos que dão suporte a ponteiros de arquivo (ou seja, dispositivos de busca), portanto, a posição do arquivo deve ser passada para as funções de leitura e gravação nos membros de dados de deslocamento relacionados da estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Para obter mais informações, consulte [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) e [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile).

A posição do ponteiro de arquivo para um identificador síncrono é mantida pelo sistema, pois os dados são lidos ou gravados e também podem ser atualizados usando a função [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) ou [**SetFilePointerEx**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex) .

Um aplicativo também pode aguardar o identificador de arquivo para sincronizar a conclusão de uma operação de e/s, mas isso requer extrema cautela. Cada vez que uma operação de e/s é iniciada, o sistema operacional define o identificador de arquivo para o estado não sinalizado. Cada vez que uma operação de e/s é concluída, o sistema operacional define o identificador de arquivo para o estado sinalizado. Portanto, se um aplicativo iniciar duas operações de e/s e aguardar o identificador do arquivo, não será possível determinar qual operação será concluída quando o identificador for definido como o estado sinalizado. Se um aplicativo precisar executar várias operações de e/s assíncronas em um único arquivo, ele deverá aguardar o identificador de evento na estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) específica para cada operação de e/s, em vez do identificador de arquivo comum.

Para cancelar todas as operações de e/s assíncronas pendentes, use:

-   [**CancelIo**](cancelio.md)– essa função cancela apenas as operações emitidas pelo thread de chamada para o identificador de arquivo especificado.
-   [**CancelIoEx**](cancelioex-func.md)– essa função cancela todas as operações emitidas pelos threads para o identificador de arquivo especificado.

Use [**CancelSynchronousIo**](cancelsynchronousio-func.md) para cancelar operações de e/s síncronas pendentes.

As funções [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) permitem que um aplicativo especifique uma rotina a ser executada (consulte [**FileIOCompletionRoutine**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)) quando a solicitação de e/s assíncrona for concluída.

 

 
