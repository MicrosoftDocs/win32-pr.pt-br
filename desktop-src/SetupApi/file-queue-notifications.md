---
description: As notificações a seguir são usadas com as filas de arquivos. Para obter mais informações sobre o formato e o uso de notificações, consulte notificações.
ms.assetid: 4a171b4a-8623-4be3-81ee-99081fe23034
title: Notificações de fila de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b674dee015c4c9408ff5dc853d5d3b2412e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011356"
---
# <a name="file-queue-notifications"></a>Notificações de fila de arquivos

As notificações a seguir são usadas com as filas de arquivos. Para obter mais informações sobre o formato e o uso de notificações, consulte [notificações](notifications.md).



| Notificação                                                      | Descrição                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)         | Ocorreu um erro durante uma operação de cópia de arquivo.                                                  |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)     | Ocorreu um erro durante uma operação de exclusão de arquivo.                                                 |
| [**SPFILENOTIFY \_ ENDcopy**](spfilenotify-endcopy.md)             | Uma operação de cópia de arquivo foi finalizada.                                                                 |
| [**SPFILENOTIFY \_ ENDdelete**](spfilenotify-enddelete.md)         | Uma operação de exclusão de arquivo foi finalizada.                                                                |
| [**SPFILENOTIFY \_ ENDqueue**](spfilenotify-endqueue.md)           | A fila concluiu a confirmação.                                                                  |
| [**\_renomear SPFILENOTIFY**](spfilenotify-endrename.md)         | Uma operação de renomeação de arquivo foi finalizada.                                                                  |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)     | Uma subfila (copiar, renomear ou excluir) terminou.                                               |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md) | O arquivo estava em uso e a operação atual foi atrasada até que o sistema seja reinicializado.       |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)   | O idioma da operação atual não corresponde ao idioma do sistema.                           |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)         | A nova mídia de origem é necessária.                                                                         |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)         | Um nó na fila de arquivos foi verificado. (Somente [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) ) |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)     | Ocorreu um erro durante uma operação de renomeação de arquivo.                                                 |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)         | Uma operação de cópia de arquivo foi iniciada.                                                                  |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)     | Uma operação de exclusão de arquivo foi iniciada.                                                                |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)       | A fila começou a ser confirmada.                                                                    |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)     | Uma operação de renomeação de arquivo foi iniciada.                                                                |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md) | Uma subfila (copiar, renomear ou excluir) foi iniciada.                                             |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)   | Já existe uma cópia do arquivo especificado no destino.                                          |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)     | Existe uma versão mais recente do arquivo especificado no destino.                                         |



 

 

 



