---
description: Se a opção de processamento de retorno msidbCustomActionTypeContinue não estiver definida, a ação personalizada deverá retornar um código de status inteiro, conforme mostrado na tabela a seguir.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valores de retorno de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3853cfeafba22cb2d479feb1e699c29bcf4b0ab7a08402245f30958cb593df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044996"
---
# <a name="custom-action-return-values"></a>Valores de retorno de ação personalizada

Se a opção de processamento de retorno **msidbCustomActionTypeContinue** não estiver definida, a ação personalizada deverá retornar um código de status inteiro, conforme mostrado na tabela a seguir.



| Valor retornado                 | Descrição                           |
|------------------------------|---------------------------------------|
| função de erro \_ \_ não \_ chamada | Ação não executada.                  |
| êxito do erro \_               | Ações concluídas com êxito.       |
| ERRO ao \_ instalar o \_ UserExit     | O usuário terminou prematuramente.          |
| \_falha na instalação do erro \_      | Ocorreu um erro irrecuperável.         |
| ERRO \_ não há \_ mais \_ itens       | Ignore as ações restantes, não um erro. |



 

Observe que as ações personalizadas que são [arquivos executáveis](executable-files.md) devem retornar um valor de 0 para êxito. O instalador interpreta qualquer outro valor de retorno como falha. Para ignorar valores de retorno, defina o sinalizador de bit **msidbCustomActionTypeContinue** no campo Type da [tabela CustomAction](customaction-table.md).

Para obter mais informações sobre a opção **msidbCustomActionTypeContinue** e outras opções de processamento de retorno, consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).

observe que Windows Installer converte os valores de retorno de todas as ações quando grava o valor de retorno no arquivo de log. Por exemplo, se o valor de retorno da ação aparecer como 1 no arquivo de log, isso significa que a ação retornou êxito de erro \_ . Para obter mais informações sobre essa conversão, consulte [log de valores de retorno de ação](logging-of-action-return-values.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de Erro](error-codes.md)
</dt> <dt>

[Registro de valores de retorno de ação](logging-of-action-return-values.md)
</dt> </dl>

 

 



