---
description: Como a API de Instalação não fornece uma rotina de retorno de chamada de gabinete padrão, você precisa fornecer uma rotina. A rotina de retorno de chamada que a função SetupIterateCabinet requer deve ter o mesmo formato que aqueles apontados por FileCallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Criando uma rotina de retorno de chamada de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8e3c396452e7684e24c141fd519f6c8ed45fe08d87933f9308e88a6e9f3ac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966040"
---
# <a name="creating-a-cabinet-callback-routine"></a>Criando uma rotina de retorno de chamada de gabinete

Como a API de Instalação não fornece uma rotina de retorno de chamada de gabinete padrão, você precisa fornecer uma rotina. A rotina de retorno de chamada que a [**função SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) requer deve ter o mesmo formato que aqueles apontados por [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).

A seguir está a sintaxe que [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) usa para enviar uma notificação para a rotina de retorno de chamada.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

O *parâmetro Context* é um ponteiro nulo para uma variável de contexto ou estrutura que pode ser usada pela rotina de retorno de chamada para armazenar informações que precisam persistir entre chamadas subsequentes para a rotina de retorno de chamada.

A implementação desse contexto é especificada pela rotina de retorno de chamada e nunca é referenciada ou alterada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

O *parâmetro* Notification é um inteiro sem sinal e será um dos valores a seguir.



| Notificação                                                        | Descrição                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)   | O arquivo foi extraído do gabinete.      |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)   | Um arquivo é encontrado no gabinete.              |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md) | O arquivo atual continua no próximo gabinete. |



 

Os dois parâmetros finais, *Param1* e *Param2,* também são inteiros sem sinal e contêm informações adicionais relevantes para a notificação. Para obter mais informações sobre as notificações enviadas por [**SetupIterateCabinet,**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)consulte [Notificações de arquivo de gabinete](cabinet-file-notifications.md).

Uma rotina DE RETORNO DE CHAMADA NOTIFICAÇÃO DE ARQUIVO \_ SP retorna um inteiro sem \_ \_ sinal. A rotina de retorno de chamada de gabinete deve retornar um dos valores a seguir, dependendo da notificação.

Para a notificação SPFILENOTIFY \_ FILEINCABINET, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) espera que um dos valores a seguir seja retornado pela rotina de retorno de chamada.



| Valor         | Significado                   |
|---------------|---------------------------|
| FILEOP \_ ABORT | Anular o processamento de gabinete. |
| FILEOP \_ DOIT  | Extraia o arquivo atual. |
| FILEOP \_ SKIP  | Ignore o arquivo atual.    |



 

Para notificações SPFILENOTIFY \_ NEEDNEWCABINET e SPFILENOTIFY \_ FILEEXTRACTED, **SetupIterateCabinet** espera que um dos valores a seguir seja retornado pela rotina de retorno de chamada.



| Valor      | Significado                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NENHUM \_ ERRO  | Nenhum erro foi encontrado, continue processando o gabinete.                                                                                                                                                                        |
| ERRO \_ XXX | Ocorreu um erro do tipo especificado. A [**função SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retornará **FALSE** e o código de erro especificado será retornado por uma chamada para [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) |



 

Se a rotina de retorno de chamada retornar \_ FILEOP DOIT, a rotina também deverá fornecer um caminho de destino completo. Para obter mais informações, [**consulte SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).

 

 
