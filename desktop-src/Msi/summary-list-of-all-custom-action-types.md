---
description: A tabela a seguir identifica os tipos básicos de ações personalizadas e mostra os valores que estão nos campos Tipo, Origem e Destino da tabela CustomAction para cada tipo.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Tipos de ação personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0be8a9465c9a3567a867bab911d7539e8700219515c86bb5a8fc2b7d5eff68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624301"
---
# <a name="custom-action-types"></a>Tipos de ação personalizados

A tabela a seguir identifica os tipos básicos de ações personalizadas e mostra os valores que estão nos campos Tipo, Origem e Destino da tabela [CustomAction](customaction-table.md) para cada tipo. As ações personalizadas básicas podem ser modificadas incluindo bits de sinalizador opcionais na coluna Tipo. Para ver descrições das opções e dos valores, confira o seguinte:

-   [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md)
-   [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md)
-   [Opções de execução In-Script ação personalizada](custom-action-in-script-execution-options.md)
-   [Opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md)

Use os links para o Tipo de Ação Personalizada Básica para uma descrição e as opções disponíveis para cada tipo.



| Tipo de ação personalizada básica                                                                                                                           | Tipo | Fonte                                                                                                                              | Destino                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo de ação personalizada 1](custom-action-type-1.md) Arquivo DLL armazenado em um fluxo de tabela binário.<br/>                                               | 1    | Chave para [tabela binária.](binary-table.md)                                                                                            | Ponto de entrada da DLL.                                                                                                                           |
| [Tipo de ação personalizada 2](custom-action-type-2.md) Arquivo EXE armazenado em um fluxo de tabela binário.<br/>                                               | 2    | Chave para [tabela binária.](binary-table.md)                                                                                            | Cadeia de caracteres de linha de comando.                                                                                                                       |
| [Tipo de ação personalizada 5](custom-action-type-5.md)JScript arquivo armazenado em um fluxo de tabela binário.<br/>                                           | 5    | Chave para [tabela binária.](binary-table.md)                                                                                            | Uma função JScript opcional que pode ser chamada.                                                                                           |
| [Tipo de ação personalizada 6](custom-action-type-6.md) Arquivo VBScript armazenado em um fluxo de tabela binário.<br/>                                          | 6    | Chave para [tabela binária.](binary-table.md)                                                                                            | Uma função opcional do VBScript que pode ser chamada.                                                                                          |
| [Tipo de ação personalizada 17](custom-action-type-17.md) Arquivo DLL instalado com um produto.<br/>                                            | 17   | Chave para [Tabela de](file-table.md) arquivos.                                                                                                | Ponto de entrada da DLL.                                                                                                                           |
| [Tipo de ação personalizada 18](custom-action-type-18.md) Arquivo EXE instalado com um produto.<br/>                                            | 18   | Chave para [Tabela de](file-table.md) arquivos.                                                                                                | Cadeia de caracteres de linha de comando.                                                                                                                       |
| [Tipo de ação personalizada 19](custom-action-type-19.md) Exibe uma mensagem de erro especificada e retorna a falha, encerrando a instalação.<br/> | 19   | Em branco                                                                                                                               | [Cadeia de caracteres](formatted.md) de texto formatada. A mensagem literal ou um índice na [tabela Erro.](error-table.md)                           |
| [Tipo de ação personalizada 21](custom-action-type-21.md)JScript arquivo instalado com um produto.<br/>                                        | 21   | Chave para [Tabela de](file-table.md) arquivos.                                                                                                | Uma função JScript opcional que pode ser chamada.                                                                                           |
| [Tipo de ação personalizada 22](custom-action-type-22.md) Arquivo VBScript instalado com um produto.<br/>                                       | 22   | Chave para [Tabela de](file-table.md) arquivos.                                                                                                | Uma função opcional do VBScript que pode ser chamada.                                                                                          |
| [Tipo de ação personalizada 34](custom-action-type-34.md) Arquivo EXE com um caminho que referencia um diretório.<br/>                                       | 34   | Chave para [a tabela](directory-table.md) Diretório. Este é o diretório de trabalho para execução.                                         | A coluna Destino é [formatada](formatted.md) e contém o caminho completo e o nome do arquivo executável seguido por argumentos opcionais. |
| [Tipo de ação personalizada 35](custom-action-type-35.md) Conjunto de diretórios com texto formatado.<br/>                                                    | 35   | Uma chave para a [tabela](directory-table.md) Diretório. O diretório designado é definido pela cadeia de caracteres formatada no campo Destino.   | Uma cadeia de caracteres de texto formatada.                                                                                                                   |
| [Tipo de Ação Personalizada 37](custom-action-type-37.md)JScript texto armazenado nesta tabela de sequência.<br/>                                           | 37   | Nulo                                                                                                                                | Uma cadeia de caracteres JScript código.                                                                                                                  |
| [Tipo de ação personalizada 38](custom-action-type-38.md) Texto VBScript armazenado nesta tabela de sequência.<br/>                                          | 38   | Nulo                                                                                                                                | Uma cadeia de caracteres de código VBScript.                                                                                                                 |
| [Tipo de ação personalizada 50](custom-action-type-50.md) Arquivo EXE com um caminho especificado por um valor de propriedade.<br/>                                 | 50   | Nome da propriedade ou chave para [a tabela](property-table.md) Propriedade.                                                                       | Cadeia de caracteres de linha de comando.                                                                                                                       |
| [Tipo de ação personalizada 51](custom-action-type-51.md) Propriedade definida com texto formatado.<br/>                                                     | 51   | Nome da propriedade ou chave para a [tabela](property-table.md) Propriedade. Essa propriedade é definida pela cadeia de caracteres formatada no campo Destino. | Uma cadeia de caracteres de texto formatada.                                                                                                                   |
| [Tipo de Ação Personalizada 53](custom-action-type-53.md)JScript texto especificado por um valor de propriedade.<br/>                                           | 53   | Nome da propriedade ou chave para [a tabela](property-table.md) Propriedade.                                                                       | Uma função JScript opcional que pode ser chamada.                                                                                           |
| [Tipo de ação personalizada 54](custom-action-type-54.md) Texto do VBScript especificado por um valor de propriedade.<br/>                                          | 54   | Nome da propriedade ou chave para [a tabela](property-table.md) Propriedade.                                                                       | Uma função opcional do VBScript que pode ser chamada.                                                                                          |



 

Além disso, os seguintes tipos de ação personalizadas são usados com instalações simultâneas:

-   [Tipo de ação personalizada 7](custom-action-type-7.md)
-   [Tipo de ação personalizada 23](custom-action-type-23.md)
-   [Tipo de ação personalizada 39](custom-action-type-39.md)

 

 




