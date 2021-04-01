---
description: Como a API de instalação não fornece uma rotina de retorno de chamada de gabinete padrão, você precisa fornecer uma rotina. A rotina de retorno de chamada que a função SetupIterateCabinet requer deve ter a mesma forma que aquelas apontadas por filecallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Criando uma rotina de retorno de chamada de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169824"
---
# <a name="creating-a-cabinet-callback-routine"></a>Criando uma rotina de retorno de chamada de gabinete

Como a API de instalação não fornece uma rotina de retorno de chamada de gabinete padrão, você precisa fornecer uma rotina. A rotina de retorno de chamada que a função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) requer deve ter a mesma forma que aquelas apontadas por [filecallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).

Veja a seguir a sintaxe que o [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) usa para enviar uma notificação para a rotina de retorno de chamada.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

O parâmetro de *contexto* é um ponteiro void para uma variável de contexto ou estrutura que pode ser usada pela rotina de retorno de chamada para armazenar informações que precisam persistir entre chamadas subsequentes para a rotina de retorno de chamada.

A implementação desse contexto é especificada pela rotina de retorno de chamada e nunca é referenciada ou alterada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

O parâmetro de *notificação* é um inteiro não assinado e será um dos valores a seguir.



| Notificação                                                        | Descrição                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**SPFILENOTIFY \_ extraied**](spfilenotify-fileextracted.md)   | O arquivo foi extraído do gabinete.      |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)   | Um arquivo é encontrado no gabinete.              |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md) | O arquivo atual continua no próximo gabinete. |



 

Os dois últimos parâmetros, *param1* e *param2*, também são inteiros sem sinal e contêm informações adicionais relevantes para a notificação. Para obter mais informações sobre as notificações enviadas pelo [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), consulte [notificação de arquivo de gabinete](cabinet-file-notifications.md).

Uma \_ rotina de \_ retorno de chamada notificar arquivo do SP \_ retorna um inteiro sem sinal. A rotina de retorno de chamada do gabinete deve retornar um dos valores a seguir, dependendo da notificação.

Para a \_ notificação SPFILENOTIFY FILEINCABINET, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) espera que um dos valores a seguir seja retornado pela rotina de retorno de chamada.



| Valor         | Significado                   |
|---------------|---------------------------|
| \_anular FILEOP | Anular o processamento do gabinete. |
| FILEOP \_ doit  | Extraia o arquivo atual. |
| FILEOP \_ ignorar  | Ignorar o arquivo atual.    |



 

Para \_ notificações SPFILENOTIFY NEEDNEWCABINET e SPFILENOTIFY extracçãod \_ , **SetupIterateCabinet** espera que um dos valores a seguir seja retornado pela rotina de retorno de chamada.



| Valor      | Significado                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEM \_ erros  | Nenhum erro foi encontrado, continue processando o gabinete.                                                                                                                                                                        |
| ERRO \_ xxx | Ocorreu um erro do tipo especificado. A função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retornará **false** e o código de erro especificado será retornado por uma chamada para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). |



 

Se a rotina de retorno de chamada retornar FILEOP \_ doit, a rotina também deverá fornecer um caminho de destino completo. Para obter mais informações, consulte [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).

 

 
