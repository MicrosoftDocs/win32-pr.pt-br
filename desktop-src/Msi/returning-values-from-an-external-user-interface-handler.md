---
description: Um manipulador de interface do usuário externo (IU) pode retornar qualquer número de valores para Windows Installer dependendo do tipo de botão fornecido no parâmetro de tipo de mensagem que o instalador passa para o manipulador.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Retornando valores de um manipulador de interface do usuário externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661557"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>Retornando valores de um manipulador de interface do usuário externo

Um manipulador de interface do usuário externo (IU) pode retornar qualquer número de valores para Windows Installer dependendo do tipo de botão fornecido no parâmetro de tipo de mensagem que o instalador passa para o manipulador.

O manipulador de interface do usuário externa pode retornar os valores – 1 e 0 a qualquer momento, pois eles não estão relacionados aos tipos de botão. Um valor de retorno de – 1 indica que ocorreu um erro interno no manipulador de interface do usuário externa. Um valor de retorno de 0 indica que o manipulador de interface do usuário externo não tratou a mensagem do instalador e o instalador deve manipular a mensagem em vez disso.

Para mensagens que não incluem um tipo de botão, como INSTALLMESSAGE \_ ACTIONDATA e INSTALLMESSAGE \_ Progress, retornar IDCANCEL cancela a instalação. Retornar IDOK notifica o instalador de que a mensagem foi tratada pelo manipulador de interface do usuário externa.

Os valores de retorno restantes, conforme descrito abaixo, estão diretamente relacionados aos tipos de botão que são incluídos com o tipo de mensagem.



| Valor de retorno da interface do usuário externa | Significado                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | O botão **OK** foi pressionado pelo usuário. As informações da mensagem foram compreendidas.                     |
| IDCANCEL                 | O botão **Cancelar** foi pressionado. Cancele a instalação.                                            |
| IDABORT                  | O botão **anular** foi pressionado. Anule a instalação.                                              |
| IDRETRY                  | O botão de **repetição** foi pressionado. Tente a ação novamente.                                                |
| IDIGNORE                 | O botão **ignorar** foi pressionado. Ignore o erro e continue.                                      |
| IDYES                    | O botão **Sim** foi pressionado. A resposta afirmativo, continue com a sequência atual de eventos..   |
| IDNO                     | O botão **não** foi pressionado. A resposta negativa não continua com a sequência de eventos atual. |



 

Por exemplo, se o manipulador da interface do usuário externa for enviado uma mensagem com o \_ sinalizador de estilos da caixa de mensagem MB ABORTRETRYIGNORE, o manipulador de interface do usuário externa poderá retornar um dos seguintes valores:

-   – 1 (erro no manipulador de interface do usuário externa)
-   0 (nenhuma ação realizada no manipulador de interface do usuário externa, permita que Windows Installer manipule-o)
-   IDABORT (botão **anular** pressionado)
-   IDRETRY (botão de **repetição** pressionado)
-   IDIGNORE (botão **ignorar** pressionado)

 

 



