---
description: Notificações são valores que uma função de instalação envia a uma rotina de retorno de chamada para especificar um Estado ou evento. Dois parâmetros, param1 e param2, são enviados com a notificação e contêm informações adicionais relevantes para a notificação.
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: Notificações (API de instalação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096d4261a99e0a837a90aa5c965a3b676843945d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755549"
---
# <a name="notifications-setup-api"></a>Notificações (API de instalação)

Notificações são valores que uma função de instalação envia a uma rotina de retorno de chamada para especificar um Estado ou evento. Dois parâmetros, *param1* e *param2*, são enviados com a notificação e contêm informações adicionais relevantes para a notificação.

A rotina de retorno de chamada processa a notificação e retorna um inteiro não assinado para a função de instalação. Dependendo da função de instalação, você pode usar esse valor para especificar uma operação ou seleção de usuário ou pode ignorá-la.

As funções de instalação enviam notificações para rotinas de retorno de chamada usando a sintaxe a seguir.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

O parâmetro de *contexto* é um ponteiro void para uma variável de contexto ou estrutura que a rotina de retorno de chamada pode usar para armazenar informações que devem persistir entre chamadas subsequentes para a rotina de retorno de chamada.

Como a rotina de retorno de chamada especifica a implementação do contexto e nunca é referenciada ou alterada pelas funções de instalação, o contexto não é documentado no material de referência para as mensagens de notificação a seguir.

O parâmetro de *notificação* especifica um valor inteiro sem sinal para um evento ou estado que faz com que a função de instalação chame a rotina de retorno de chamada.

*Param1* e *param2* são parâmetros opcionais que podem conter informações adicionais relevantes para a notificação. Esses parâmetros são inteiros sem sinal. Se *param1* ou *param2* retornar informações que não sejam um inteiro não assinado, ele será convertido em um inteiro não assinado e deverá ser reconvertido em seu tipo de dados original antes que possa ser usado pela rotina de retorno de chamada.

> [!Note]  
> As notificações a seguir representam todas as notificações usadas pelas funções de instalação. As funções individuais usam um subconjunto dessas notificações. Em outras palavras, nem todas as notificações são usadas por cada função.

 

As notificações a seguir são usadas pelas funções de instalação.



| Notificação                                                                     | Descrição                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)                        | Ocorreu um erro durante uma operação de cópia de arquivo.                                               |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)                    | Ocorreu um erro durante uma operação de exclusão de arquivo.                                           |
| [**SPFILENOTIFY \_ ENDcopy**](spfilenotify-endcopy.md)                            | Uma operação de cópia de arquivo foi finalizada.                                                              |
| [**SPFILENOTIFY \_ ENDdelete**](spfilenotify-enddelete.md)                        | Uma operação de exclusão de arquivo foi finalizada.                                                          |
| [**SPFILENOTIFY \_ ENDqueue**](spfilenotify-endqueue.md)                          | A fila concluiu a confirmação.                                                            |
| [**SPFILENOTIFY \_ ENDregistro**](spfilenotify-endregistration.md)            | O registro ou o cancelamento do registro do arquivo foi concluído.                                  |
| [**\_renomear SPFILENOTIFY**](spfilenotify-endrename.md)                        | Uma operação de renomeação de arquivo foi finalizada.                                                            |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)                    | Uma subfila (copiar, renomear ou excluir) terminou.                                         |
| [**SPFILENOTIFY \_ extraied**](spfilenotify-fileextracted.md)                | O arquivo foi extraído do gabinete.                                                 |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)                | Um arquivo é encontrado no gabinete.                                                         |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md)                | O arquivo estava em uso e a operação atual foi atrasada até que o sistema seja reinicializado. |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)                  | O idioma da operação atual não corresponde ao idioma do sistema.                     |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)                        | A nova mídia de origem é necessária.                                                                 |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md)              | O arquivo atual continua no próximo gabinete.                                            |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)                        | Um nó na fila de arquivos foi verificado.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ ex**](spfilenotify-queuescan-ex.md)                 | Um nó na fila de arquivos foi verificado.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO**](spfilenotify-queuescan-signerinfo.md) | Um nó na fila de arquivos foi verificado.                                                    |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)                    | Ocorreu um erro durante uma operação de renomeação de arquivo.                                             |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)                        | Uma operação de cópia de arquivo foi iniciada.                                                            |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)                    | Uma operação de exclusão de arquivo foi iniciada.                                                          |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)                      | A fila começou a ser confirmada.                                                              |
| [**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)        | O registro ou o cancelamento do registro do arquivo foi iniciado.                                   |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)                    | Uma operação de renomeação de arquivo foi iniciada.                                                          |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md)                | Uma subfila (copiar, renomear ou excluir) foi iniciada.                                       |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)                  | Já existe uma cópia do arquivo especificado no destino.                                    |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)                    | Existe uma versão mais recente do arquivo especificado no destino.                                   |



 

 

 



