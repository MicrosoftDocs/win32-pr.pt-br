---
title: Srdelayed.exe
description: Os aplicativos que executam operações de restauração de estado do sistema no início da inicialização do sistema operacional podem não conseguir usar as funções de gerenciamento de arquivos para mover, excluir ou definir o nome curto de determinados arquivos do sistema.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Srdelayed.exe backup
- backup de recuperação de estado do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdf95ff77fd17a578b85e6037c71146666eae9522d066bc1c4629fb9a2c24e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835534"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Os aplicativos que executam operações de restauração de estado do sistema no início da inicialização do sistema operacional podem não conseguir usar as funções de gerenciamento de arquivos para mover, excluir ou definir o nome curto de determinados arquivos do sistema. Srdelayed.exe é um arquivo executável, fornecido com o recurso WSB (Backup do Servidor do Windows) no Windows Server 2008, que pode habilitar aplicativos de recuperação de estado do sistema para mover, excluir e definir o nome curto dos arquivos do sistema.

A ferramenta Slayedlayed destina-se a aplicativos de recuperação de estado do sistema; ele não substitui as funções de gerenciamento de arquivos. Essa ferramenta deve ser usada somente quando o aplicativo não puder mover, excluir ou definir o nome curto de um arquivo do sistema usando as funções [**MoveFileEx,**](/windows/desktop/api/winbase/nf-winbase-movefileexa) [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)e [**SetFileShortName.**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) Durante uma restauração e reinicialização de estado do sistema, Srdelayed.exe é usado pelo Restauração do Sistema e pela ferramenta de linha de comando wbadmin.exe para mover, excluir e definir o nome curto em determinados arquivos do sistema. Portanto, o Sabellayed pode ser útil para desenvolvedores que exigem a capacidade de restaurar esses arquivos do sistema em seus próprios aplicativos de recuperação de estado do sistema.

O Sárialayed pode executar as seguintes operações:

-   Uma operação de movimentação de arquivo semelhante à [**função MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) com o **sinalizador MOVEFILE DELAY UNTIL \_ \_ \_ REBOOT**
-   Uma operação de exclusão de arquivo semelhante à [**função DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)
-   Uma operação de nome curto definida semelhante à [**função SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea)

Para usar Oaslayed, seu aplicativo requer o caminho completo para o local do arquivo Srdelayed.exe e o caminho completo para um arquivo de texto Unicode que você tenha sido autor para conter as informações que a ferramenta precisa para executar todas as operações de gerenciamento de arquivos que estão sendo solicitadas. Seu aplicativo é responsável por garantir que esse arquivo de texto não contenha solicitações redundantes para uma operação e que ele trata qualquer ordenação necessária das operações de gerenciamento de arquivos. Por exemplo, como uma pasta deve estar vazia para ser excluída, seu aplicativo precisa garantir que o arquivo de texto especifique a remoção de todos os arquivos dentro da pasta antes de solicitar que a pasta seja excluída.

Se a entrada **SetupExecute** ainda não existir no Registro, seu aplicativo precisará criar uma entrada de tipo **REG MULTI \_ \_ SZ** chamada **SetupExecute** na seguinte chave do Registro: **HKEY LOCAL \_ \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**.

Seu aplicativo deve usar o seguinte formato para definir o valor de **SetupExecute** como o caminho completo para o local do arquivo Srdelayed.exe e o caminho completo para o local do arquivo de texto. Prefixo " \\ \\ ?? \\ " para o caminho do arquivo de texto, da seguinte forma:

*Caminho completo para Srdelayed.exe* \\ \\ ?? \\ *Caminho completo para o arquivo de texto*  


Por exemplo, o seguinte valor para **SetupExecute** indica que o Srdelayed.exe está localizado na pasta System32 e o arquivo de texto é denominado DelayedOperations:

C: \\ Windows \\ System32 \\srdelayed.exe \\ \\ ?? \\ C: \\ temp \\ DelayedOperations  


Os espaços no caminho e no nome devem ser codificados hexadecimais. Por exemplo, para *Arquivos de Programas*, codificar o caminho como " \\ \\ ?? \\ C:Program%20Files \\a.dll".

Quando o registro ou o sistema está sendo restaurado após a reinicialização, seu aplicativo precisa garantir que **SetupExecute** seja gravado no hive do Registro correto. A recuperação do Registro é executada antes Srdelayed.exe é executado. O aplicativo precisa gravar **SetupExecute** na versão recuperada do Registro porque essa é a versão lida.

## <a name="format-for-the-srdelayed-input-file"></a>Formato para o arquivo de entrada Slayed

Todas as informações necessárias para executar operações de gerenciamento de arquivos são especificadas como uma cadeia de caracteres Unicode em um arquivo de texto Unicode. A cadeia de caracteres Unicode é particionada em registros que são particionados em quatro campos. Cada registro especifica um único arquivo de movimentação, excluir arquivo ou definir operação de nome curto. Os quatro campos de cada registro contêm os parâmetros para a operação. Srdelayed.exe executa cada operação na ordem em que seus registros ocorrem na cadeia de caracteres. Seu aplicativo deve verificar se há registros duplicados nesse arquivo e remover as duplicatas.

A cadeia de caracteres a seguir ilustra o formato de um arquivo que solicita duas operações e consiste em dois registros. Cada campo de parâmetro termina com um único caractere de \\ L' 0'. Um registro é composto por quatro campos consecutivos. Um caractere L' \\ 0' adicional é anexado ao final de todos os registros.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


O significado dos campos de primeiro, segundo, terceiro e quarto parâmetros depende se o registro descreve uma operação de movimentação, exclusão ou definição de nome curto.

## <a name="format-for-a-move-file-record"></a>Formato para um registro de arquivo de movimentação

O campo 1 identifica isso como uma solicitação para mover um arquivo. O valor nesse campo é sempre L"MoveFile" e é sensível a minúsculas.

O campo 2 especifica o local de origem do arquivo. A operação de arquivo de movimentação Slayed não dá suporte à movimentação de uma pasta. Um arquivo deve ser especificado neste campo. O valor desse campo é o caminho completo do arquivo anexado a " ?? ", a menos que o caminho inclua um \\ \\ \\ GUID (identificador global exclusivo), que usa " ? " como \\ \\ \\ prefixo. Remova " \\ \\ ? " antes de fazer \\ a adoção de " \\ \\ ?? \\ ".

O campo 3 especifica o destino do arquivo. A operação de movimentação de arquivo só funciona dentro de um volume. A origem e o destino devem estar no mesmo volume. O valor desse campo é o caminho completo do arquivo anexado a " ?? ", a menos que o caminho inclua um \\ \\ \\ GUID (identificador global exclusivo), que usa " ? " como \\ \\ \\ prefixo. Remova " \\ \\ ? " antes de fazer \\ a adoção de " \\ \\ ?? \\ ".

O campo 4 recebe informações de status de Slayed. O valor nesse campo deve ser definido como L"NotExecuted" para um novo registro.

O exemplo a seguir faz referência ao arquivo por caminho da unidade. Se o caminho e o nome da origem for C: Estágioa.dll, esse registro solicitará que Slayedlayed mova-o para \\ \\ C: \\ temp \\a.dll.

MoveFile \\ \\ ?? \\ C: \\ Estágio \\a.dll \\ \\ ?? \\ C: \\ temp \\a.dll NotExecuted  


O exemplo a seguir faz referência ao caminho guid do arquivo por volume. Se o caminho e o nome da origem for \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} Stagea.dll, esse registro solicita que \\ Slayedlayed mova-o \\ para \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll

 MoveFile \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ Estágio \\a.dll \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll NotExecuted  


## <a name="format-for-a-delete-file-record"></a>Formato para um registro de arquivo de exclusão

O campo 1 identifica isso como uma solicitação para excluir um arquivo. O valor nesse campo é sempre L"DeleteFile" e é sensível a minúsculas.

O campo 2 não está sendousado. O valor nesse campo deve ser definido como L"Unused".

O campo 3 especifica o arquivo a ser removido. Uma pasta deve estar vazia para ser removida. Use operações de exclusão de arquivo para remover todos os arquivos na pasta antes de remover a pasta. O valor desse campo é o caminho completo do arquivo anexado a " ?? ", a menos que o caminho inclua um \\ \\ \\ GUID (identificador global exclusivo), que usa " ? " como \\ \\ \\ prefixo. Remova " \\ \\ ? " antes de fazer \\ a adoção de " \\ \\ ?? \\ ".

O campo 4 recebe informações de status de Slayed. O valor nesse campo deve ser definido como L"NotExecuted" para um novo registro.

O exemplo a seguir faz referência ao arquivo por caminho da unidade. Se o caminho e o nome for C: tempb.dll, esse registro solicitará que \\ \\ Slayed exclua o arquivo.

DeleteFile Unused \\ \\ ?? \\ C: \\ temp \\b.dll NotExecuted  


O exemplo a seguir faz referência ao GUID de arquivo por volume. Se o caminho e o nome for \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} tempb.dll, esse registro solicita que \\ \\ Slayedlayed remova o arquivo.

DeleteFile Unused \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll\\ NotExecuted  


## <a name="format-for-set-short-name-record"></a>Formato para Definir Short-Name Registro

O campo 1 identifica isso como uma solicitação para definir o nome curto de um arquivo. O valor nesse campo é sempre L"SetFileShortName" e é sensível a minúsculas.

O campo 2 especifica o nome curto.

O campo 3 especifica o caminho e o nome longo para receber o nome curto. O valor desse campo é o caminho e o nome longo do arquivo anexado a " ?? ", a menos que o caminho inclua um \\ \\ \\ GUID (identificador global exclusivo), que usa " ? " como \\ \\ \\ prefixo. Remova " \\ \\ ? " antes de fazer \\ a adoção de " \\ \\ ?? \\ ".

O campo 4 recebe informações de status de Slayed. O valor nesse campo deve ser definido como L"NotExecuted" para um novo registro.

O exemplo a seguir faz referência ao arquivo por caminho da unidade. Se o caminho e o nome do arquivo for C: tempShortFileName.dll, esse registro solicitará que o arquivo receba um nome \\ \\ curto, ShortN~1.dll.

SetFileShortName ShortN~1.dll \\ \\ ?? \\ C: \\ temp \\ShortFileName.dll NotExecuted  


O exemplo a seguir faz referência ao GUID de arquivo por volume. Se o caminho e o nome do arquivo for \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} tempShortFileName.dll, esse registro solicita que o arquivo receba um nome \\ \\ \\ curto, ShortN~1.dll.

SetFileShortName ShortN~1.dll \\ \\ ?? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ NotExecuted  


## <a name="srdelayed-operations-status"></a>Status de operações atrasadas

Snixlayed grava a cadeia de caracteres L"SC=*xxxxxxx*" no quarto campo de cada registro do arquivo de texto, em que *xxxxxxx* é um hexadecimal que indica o status da operação solicitada. Um valor de zero indica que a operação foi bem-sucedida.

Sarialayed cria uma chave do Registro chamada **SystemRestore** em **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** para registrar o resultado de toda a operação de restauração. Se Stimalayed executar todas as operações solicitadas com êxito, o nome RestoreStatusResult será gravado sob essa chave com um valor zero. Se Srdelayed não puder executar nenhuma das operações solicitadas, os nomes RestoreStatusResult e RestoreStatusDetails serão gravados sob essa chave com valores diferentes de zero. O nome RestoreStatusDetails será gravado sob essa chave somente se Srdelayed não puder executar nenhuma operação solicitada. Se uma operação para definir o nome curto de um arquivo não for bem-sucedida, o Srdelayed continuará para a próxima operação. Srdelayed considera as operações Mover arquivo e excluir arquivo como críticas e não continua se uma operação de movimentação ou exclusão não for bem-sucedida.

 

 