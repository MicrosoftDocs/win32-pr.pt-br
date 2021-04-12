---
title: Srdelayed.exe
description: Os aplicativos que executam operações de restauração de estado do sistema no início da inicialização do sistema operacional podem não ser capazes de usar as funções de gerenciamento de arquivos para mover, excluir ou definir o nome curto de determinados arquivos do sistema.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Srdelayed.exe backup
- Backup de recuperação de estado do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5f6b281c07f5b0ad8d6cd7e59b4f93ec9208a5
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104454430"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Os aplicativos que executam operações de restauração de estado do sistema no início da inicialização do sistema operacional podem não ser capazes de usar as funções de gerenciamento de arquivos para mover, excluir ou definir o nome curto de determinados arquivos do sistema. Srdelayed.exe é um arquivo executável, fornecido com o recurso Backup do Windows Server (WSB) no Windows Server 2008, que pode permitir que os aplicativos de recuperação de estado do sistema movam, excluam e definam o nome curto dos arquivos do sistema.

A ferramenta Srdelayed é destinada a aplicativos de recuperação de estado do sistema; Ele não substitui as funções de gerenciamento de arquivos. Essa ferramenta deve ser usada somente quando o aplicativo não puder mover, excluir ou definir o nome curto de um arquivo do sistema usando as funções [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa), [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)e [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) . Durante uma restauração e reinicialização do estado do sistema, Srdelayed.exe é usado pela restauração do sistema e pela ferramenta de linha de comando wbadmin.exe para mover, excluir e definir o nome curto em determinados arquivos do sistema. O Srdelayed pode, portanto, ser útil para os desenvolvedores que exigem a capacidade de restaurar esses arquivos de sistema em seus próprios aplicativos de recuperação de estado do sistema.

O Srdelayed pode executar as seguintes operações:

-   Uma operação mover arquivo semelhante à função [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) com o **atraso MoveFile até o sinalizador de \_ \_ \_ reinicialização**
-   Uma operação excluir arquivo semelhante à função [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)
-   Uma operação de definição de nome curto semelhante à função [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea)

Para usar o Srdelayed, seu aplicativo requer o caminho completo para o local do arquivo de Srdelayed.exe e o caminho completo para um arquivo de texto Unicode que você criou para conter as informações de que a ferramenta precisa para executar todas as operações de gerenciamento de arquivos que estão sendo solicitadas. Seu aplicativo é responsável por garantir que esse arquivo de texto não contenha solicitações redundantes para uma operação e que ele manipule qualquer ordem necessária das operações de gerenciamento de arquivos. Por exemplo, como uma pasta deve estar vazia para ser excluída, seu aplicativo precisa garantir que o arquivo de texto especifique a remoção de todos os arquivos dentro da pasta antes de solicitar que a pasta seja excluída.

Se a entrada **SetupExecute** ainda não existir no registro, seu aplicativo precisará criar uma entrada de tipo **reg \_ multi \_ sz** denominada **SetupExecute** na seguinte chave do registro: **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**.

Seu aplicativo deve usar o formato a seguir para definir o valor de **SetupExecute** como o caminho completo para o local do arquivo de Srdelayed.exe e o caminho completo para o local do arquivo de texto. Prefix " \\ \\ ?? \\ " para o caminho do arquivo de texto, da seguinte maneira:

*Caminho completo para Srdelayed.exe* \\ \\ ?? \\ *Caminho completo para o arquivo de texto*  


Por exemplo, o valor a seguir para **SetupExecute** indica que o Srdelayed.exe está localizado na pasta system32 e o arquivo de texto é chamado DelayedOperations:

C: \\ Windows \\ System32 \\srdelayed.exe \\ \\ ?? \\ C: \\ temp \\ DelayedOperations  


Os espaços no caminho e no nome devem ser codificados em hexadecimal. Por exemplo, para *arquivos de programas*, codifique o caminho como " \\ \\ ?? \\ C:Program%20Files \\a.dll ".

Quando o registro ou sistema está sendo restaurado após a reinicialização, seu aplicativo precisa garantir que o **SetupExecute** seja gravado no hive correto do registro. A recuperação do registro é executada antes da execução do Srdelayed.exe. O aplicativo precisa gravar **SetupExecute** na versão recuperada do registro, pois essa é a versão que é lida.

## <a name="format-for-the-srdelayed-input-file"></a>Formato para o arquivo de entrada Srdelayed

Todas as informações que o Srdelayed precisa para executar operações de gerenciamento de arquivos são especificadas como uma cadeia de caracteres Unicode em um arquivo de texto Unicode. A cadeia de caracteres Unicode é particionada em registros que, por sua só, são particionados em quatro campos. Cada registro especifica uma única operação mover arquivo, excluir arquivo ou definir nome curto. Os quatro campos de cada registro contêm os parâmetros para a operação. Srdelayed.exe executa cada operação na ordem em que seus registros ocorrem na cadeia de caracteres. Seu aplicativo deve verificar se há registros duplicados nesse arquivo e remover as duplicatas.

A cadeia de caracteres a seguir ilustra o formato de um arquivo que solicita duas operações e que consiste em dois registros. Cada campo de parâmetro termina com um único caractere L ' \\ 0 '. Um registro é composto de quatro campos consecutivos. Um único caractere L ' \\ 0 ' adicional é acrescentado ao final de todos os registros.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


O significado dos primeiros, segundo, terceiro e quarto campos de parâmetro depende se o registro descreve uma operação de movimentação, exclusão ou definição de nome curto.

## <a name="format-for-a-move-file-record"></a>Formato de um registro de arquivo de movimentação

O campo 1 identifica isso como uma solicitação para mover um arquivo. O valor neste campo é sempre L "MoveFile" e diferencia maiúsculas de minúsculas.

O campo 2 especifica o local de origem do arquivo. A operação Srdelayed mover arquivo não dá suporte à movimentação de uma pasta. Um arquivo deve ser especificado neste campo. O valor desse campo é o caminho completo do arquivo anexado a " \\ \\ ?? \\ ", a menos que o caminho inclua um identificador global exclusivo (GUID), que usa " \\ \\ ? \\ " como um prefixo. Remover " \\ \\ ? \\ " antes de anexar a " \\ \\ ?? \\ ".

O campo 3 especifica o destino do arquivo. A operação mover arquivo funciona apenas dentro de um volume. A origem e o destino devem estar no mesmo volume. O valor desse campo é o caminho completo do arquivo anexado a " \\ \\ ?? \\ ", a menos que o caminho inclua um identificador global exclusivo (GUID), que usa " \\ \\ ? \\ " como um prefixo. Remover " \\ \\ ? \\ " antes de anexar a " \\ \\ ?? \\ ".

O campo 4 recebe informações de status de Srdelayed. O valor neste campo deve ser definido como L "não executado" para um novo registro.

O exemplo a seguir faz referência ao arquivo pelo caminho da unidade. Se o caminho e o nome da origem forem C: \\ Stage \\a.dll, esse registro solicitará que Srdelayed mova-o para C: \\ temp \\a.dll.

MoveFile \\ \\ ?? \\ C: \\ estágio \\a.dll \\ \\ ?? \\ C: \\ temp \\a.dll não executado  


O exemplo a seguir referencia o arquivo por caminho de GUID de volume. Se o caminho e o nome da origem forem \\ \\ ? \\ O volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ Stage \\a.dll, este registro solicita que Srdelayed mova-o para \\ \\ ? \\a.dll Temp do volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ \\

 MoveFile \\ \\ ?? \\ O estágio do volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ \\a.dll \\ \\ ?? \\ Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\a.dll não executado  


## <a name="format-for-a-delete-file-record"></a>Formato de um registro de arquivo de exclusão

O campo 1 identifica isso como uma solicitação para excluir um arquivo. O valor neste campo é sempre L "DeleteFile" e diferencia maiúsculas de minúsculas.

O campo 2 não é usado. O valor neste campo deve ser definido como L "não utilizado".

O campo 3 especifica o arquivo a ser removido. Uma pasta deve estar vazia para ser removida. Use excluir operações de arquivo para remover todos os arquivos na pasta antes de remover a pasta. O valor desse campo é o caminho completo do arquivo anexado a " \\ \\ ?? \\ ", a menos que o caminho inclua um identificador global exclusivo (GUID), que usa " \\ \\ ? \\ " como um prefixo. Remover " \\ \\ ? \\ " antes de anexar a " \\ \\ ?? \\ ".

O campo 4 recebe informações de status de Srdelayed. O valor neste campo deve ser definido como L "não executado" para um novo registro.

O exemplo a seguir faz referência ao arquivo pelo caminho da unidade. Se o caminho e o nome forem C: \\ temp \\b.dll, esse registro solicitará que Srdelayed exclua o arquivo.

Excluirfile não utilizado \\ \\ ?? \\ C: \\ temp \\b.dll não executado  


O exemplo a seguir faz referência ao arquivo por GUID de volume. Se o caminho e o nome forem \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dll, esse registro solicita que Srdelayed remova o arquivo.

Excluirfile não utilizado \\ \\ ?? \\ Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\b.dllnão \\ executado  


## <a name="format-for-set-short-name-record"></a>Formato para o registro de Short-Name definido

O campo 1 identifica isso como uma solicitação para definir o nome curto de um arquivo. O valor neste campo é sempre L "SetFileShortName" e diferencia maiúsculas de minúsculas.

O campo 2 especifica o nome curto.

O campo campo 3 especifica o caminho e o nome longo para receber o nome curto. O valor desse campo é o caminho e o nome longo do arquivo anexado a " \\ \\ ?? \\ ", a menos que o caminho inclua um GUID (identificador global exclusivo), que usa " \\ \\ ? \\ " como um prefixo. Remover " \\ \\ ? \\ " antes de anexar a " \\ \\ ?? \\ ".

O campo 4 recebe informações de status de Srdelayed. O valor neste campo deve ser definido como L "não executado" para um novo registro.

O exemplo a seguir faz referência ao arquivo pelo caminho da unidade. Se o caminho e o nome do arquivo forem C: \\ temp \\ShortFileName.dll, esse registro solicitará que o arquivo receba um nome curto, menor que ~1.dll.

SetFileShortName curto ~1.dll \\ \\ ?? \\ C: \\ temp \\ShortFileName.dll não executado  


O exemplo a seguir faz referência ao arquivo por GUID de volume. Se o caminho e o nome do arquivo forem \\ \\ ? \\ Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ , esse registro solicita que o arquivo receba um nome curto, menor que ~1.dll.

SetFileShortName curto ~1.dll \\ \\ ?? \\ Volume {26a21bda-a627-11d7-9931-806e6f6e6963} \\ temp \\ShortFileName.dllnão \\ executado  


## <a name="srdelayed-operations-status"></a>Status de operações do Srdelayed

Srdelayed grava a cadeia de caracteres L "SC =*xxxxxxx*" no quarto campo de cada registro do arquivo de texto, em que *xxxxxxx* é um hexadecimal que indica o status da operação solicitada. Um valor de zero indica que a operação foi bem-sucedida.

Srdelayed cria uma chave do registro chamada **SystemRestore** em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** para registrar o resultado de toda a operação de restauração. Se Srdelayed executar todas as operações solicitadas com êxito, o nome RestoreStatusResult será gravado sob essa chave com um valor zero. Se Srdelayed não puder executar nenhuma das operações solicitadas, os nomes RestoreStatusResult e RestoreStatusDetails serão gravados sob essa chave com valores diferentes de zero. O nome RestoreStatusDetails será gravado sob essa chave somente se Srdelayed não puder executar nenhuma operação solicitada. Se uma operação para definir o nome curto de um arquivo não for bem-sucedida, o Srdelayed continuará para a próxima operação. Srdelayed considera as operações Mover arquivo e excluir arquivo como críticas e não continua se uma operação de movimentação ou exclusão não for bem-sucedida.

 

 