---
description: Este tópico identifica os sinalizadores de opção que você pode usar para controlar o processamento do thread de ação personalizada.
ms.assetid: a09b3a0e-564e-41aa-af0d-2e46776f291b
title: Opções de processamento de retorno de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8664ff489280993a7fc52117f3d19bccb023b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837320"
---
# <a name="custom-action-return-processing-options"></a>Opções de processamento de retorno de ação personalizada

Este tópico identifica os sinalizadores de opção que você pode usar para controlar o processamento do thread de ação personalizada. Os sinalizadores são usados para especificar que os threads de ação principal e personalizada sejam executados de forma síncrona (Windows Installer aguarda a conclusão do thread de ação personalizada antes de retomar o thread de instalação principal) ou de maneira assíncrona (Windows Installer executa a ação personalizada simultaneamente enquanto a instalação principal continua).

Para habilitar os sinalizadores de opção, adicione o valor identificado na tabela a seguir ao valor no campo tipo da [tabela CustomAction](customaction-table.md).



| Constante                                                           | Hexadecimal             | Decimal | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|-------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nenhum)                                                             | 0x00000000              | +0      | Uma execução síncrona que falhará se o código de saída não for 0 (zero). <br/> Se o sinalizador msidbCustomActionTypeContinue não estiver definido, a ação personalizada deverá retornar um dos valores de retorno descritos em [valores de retorno de ação personalizada](custom-action-return-values.md).<br/>                                                                                                                                                                                                                             |
| **msidbCustomActionTypeContinue**                                  | 0x00000040              | + 64     | Uma execução síncrona que ignora o código de saída e continua.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **msidbCustomActionTypeAsync**                                     | 0x00000080              | + 128    | Uma execução assíncrona que aguarda o código de saída no final da sequência.<br/> Essa opção não pode ser usada com [instalações simultâneas](concurrent-installations.md), [reversão de ações personalizadas](rollback-custom-actions.md)ou [ações personalizadas de script](scripts.md).<br/>                                                                                                                                                                                                                                |
| **msidbCustomActionTypeAsync**  +  **msidbCustomActionTypeContinue** | 0x00000040 + 0x00000080 | + 192    | Uma execução assíncrona que não aguarda a conclusão.<br/> A execução continua após a Windows Installer ser encerrada.<br/> Essa opção só pode ser usada com as ações personalizadas do tipo EXE, que são [arquivos executáveis](executable-files.md). <br/> Todos os outros tipos de ações personalizadas podem ser assíncronos somente na sessão de instalação e devem terminar para que a instalação seja encerrada.<br/> Esta opção não pode ser usada com [instalações simultâneas](concurrent-installations.md).<br/> |



 

 

 




