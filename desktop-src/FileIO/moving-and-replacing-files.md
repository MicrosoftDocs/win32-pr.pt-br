---
description: Considerações para mover e substituir arquivos usando as funções CopyFileEx, CreateFile, ReplaceFile e MoveFileEx.
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: Movendo e substituindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c78085865006d1dfbbe322239c4704d215d038897b81d1f139d66d06f65bbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696006"
---
# <a name="moving-and-replacing-files"></a>Movendo e substituindo arquivos

Antes que uma operação de cópia possa ser executada, o arquivo de origem deve ser fechado ou aberto somente para leitura. Nenhum thread pode ter o arquivo de origem aberto para gravação. Para copiar um arquivo existente para um novo, use a função [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) ou [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) . Os aplicativos poderão especificar se **CopyFile** e **CopyFileEx** falharão se o arquivo de destino já existir. Se o arquivo de destino existir e estiver aberto, ele deverá ter sido aberto com as permissões de compartilhamento aplicáveis. Para obter mais informações, consulte [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

A função [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) também permite que um aplicativo especifique o endereço de uma função de retorno de chamada (consulte [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)) que é chamado cada vez que outra parte do arquivo é copiada. O aplicativo pode usar essas informações para exibir um indicador que mostra o número total de bytes copiados como uma porcentagem do tamanho total do arquivo.

A função [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) substitui um arquivo por outro arquivo, com a opção de criar uma cópia de backup do arquivo original. A função preserva os atributos do arquivo original, como seu tempo de criação, ACLs e atributo de criptografia.

Um arquivo também deve ser fechado antes que um aplicativo possa movê-lo. As funções [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) e [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) copiam um arquivo existente para um novo local e exclui o original.

A função [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) também permite que um aplicativo especifique como mover o arquivo. A função pode substituir um arquivo existente, mover um arquivo entre volumes e atrasar a movimentação do arquivo até que o sistema operacional seja reiniciado.

 

 



