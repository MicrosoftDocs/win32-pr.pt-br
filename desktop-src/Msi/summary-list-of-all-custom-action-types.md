---
description: A tabela a seguir identifica os tipos básicos de ações personalizadas e mostra os valores que estão nos campos tipo, origem e destino da tabela CustomAction para cada tipo.
ms.assetid: 8713451e-c0e7-4bec-bfb6-dfe4125d5a44
title: Tipos de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5b10ffd42d2f6fecf06e0732a8960c84bea2e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837108"
---
# <a name="custom-action-types"></a>Tipos de ação personalizada

A tabela a seguir identifica os tipos básicos de ações personalizadas e mostra os valores que estão nos campos tipo, origem e destino da tabela [CustomAction](customaction-table.md) para cada tipo. As ações personalizadas básicas podem ser modificadas incluindo bits de sinalizador opcionais na coluna tipo. Para obter descrições das opções e dos valores, consulte o seguinte:

-   [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md)
-   [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md)
-   [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md)
-   [Opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md)

Use os links para o tipo de ação personalizada básica para uma descrição e as opções disponíveis para cada tipo.



| Tipo de ação personalizada básica                                                                                                                           | Tipo | Fonte                                                                                                                              | Destino                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo de ação personalizada 1](custom-action-type-1.md) Arquivo DLL armazenado em um fluxo de tabela binária.<br/>                                               | 1    | Chave para tabela [binária](binary-table.md) .                                                                                            | Ponto de entrada de DLL.                                                                                                                           |
| [Tipo de ação personalizada 2](custom-action-type-2.md) Arquivo EXE armazenado em um fluxo de tabela binária.<br/>                                               | 2    | Chave para tabela [binária](binary-table.md) .                                                                                            | Cadeia de caracteres de linha de comando.                                                                                                                       |
| [Tipo de ação personalizada 5](custom-action-type-5.md) Arquivo JScript armazenado em um fluxo de tabela binária.<br/>                                           | 5    | Chave para tabela [binária](binary-table.md) .                                                                                            | Uma função JScript opcional que pode ser chamada.                                                                                           |
| [Tipo de ação personalizada 6](custom-action-type-6.md) Arquivo VBScript armazenado em um fluxo de tabela binária.<br/>                                          | 6    | Chave para tabela [binária](binary-table.md) .                                                                                            | Uma função VBScript opcional que pode ser chamada.                                                                                          |
| [Tipo de ação personalizada 17](custom-action-type-17.md) Arquivo DLL que é instalado com um produto.<br/>                                            | 17   | Chave para a tabela de [arquivos](file-table.md) .                                                                                                | Ponto de entrada de DLL.                                                                                                                           |
| [Tipo de ação personalizada 18](custom-action-type-18.md) Arquivo EXE instalado com um produto.<br/>                                            | 18   | Chave para a tabela de [arquivos](file-table.md) .                                                                                                | Cadeia de caracteres de linha de comando.                                                                                                                       |
| [Tipo de ação personalizada 19](custom-action-type-19.md) Exibe uma mensagem de erro especificada e retorna uma falha, encerrando a instalação.<br/> | 19   | Em branco                                                                                                                               | Cadeia de texto [formatada](formatted.md) . A mensagem literal ou um índice na tabela de [erros](error-table.md) .                           |
| [Tipo de ação personalizada 21](custom-action-type-21.md) Arquivo JScript instalado com um produto.<br/>                                        | 21   | Chave para a tabela de [arquivos](file-table.md) .                                                                                                | Uma função JScript opcional que pode ser chamada.                                                                                           |
| [Tipo de ação personalizada 22](custom-action-type-22.md) Arquivo VBScript instalado com um produto.<br/>                                       | 22   | Chave para a tabela de [arquivos](file-table.md) .                                                                                                | Uma função VBScript opcional que pode ser chamada.                                                                                          |
| [Tipo de ação personalizada 34](custom-action-type-34.md) Arquivo EXE com um caminho fazendo referência a um diretório.<br/>                                       | 34   | Chave para a tabela de [diretórios](directory-table.md) . Esse é o diretório de trabalho para execução.                                         | A coluna de destino é [formatada](formatted.md) e contém o caminho completo e o nome do arquivo executável seguido por argumentos opcionais. |
| [Tipo de ação personalizada 35](custom-action-type-35.md) Conjunto de diretórios com texto formatado.<br/>                                                    | 35   | Uma chave para a tabela de [diretórios](directory-table.md) . O diretório designado é definido pela cadeia de caracteres formatada no campo de destino.   | Uma cadeia de texto formatada.                                                                                                                   |
| [Tipo de ação personalizada 37](custom-action-type-37.md) Texto JScript armazenado nesta tabela de sequência.<br/>                                           | 37   | Nulo                                                                                                                                | Uma cadeia de caracteres de código JScript.                                                                                                                  |
| [Tipo de ação personalizada 38](custom-action-type-38.md) Texto VBScript armazenado nesta tabela de sequência.<br/>                                          | 38   | Nulo                                                                                                                                | Uma cadeia de caracteres de código VBScript.                                                                                                                 |
| [Tipo de ação personalizada 50](custom-action-type-50.md) Arquivo EXE com um caminho especificado por um valor de propriedade.<br/>                                 | 50   | Nome da propriedade ou chave para a tabela de [Propriedades](property-table.md) .                                                                       | Cadeia de caracteres de linha de comando.                                                                                                                       |
| [Tipo de ação personalizada 51](custom-action-type-51.md) Conjunto de propriedades com texto formatado.<br/>                                                     | 51   | Nome da propriedade ou chave para a tabela de [Propriedades](property-table.md) . Essa propriedade é definida pela cadeia de caracteres formatada no campo de destino. | Uma cadeia de texto formatada.                                                                                                                   |
| [Tipo de ação personalizada 53](custom-action-type-53.md) Texto JScript especificado por um valor de propriedade.<br/>                                           | 53   | Nome da propriedade ou chave para a tabela de [Propriedades](property-table.md) .                                                                       | Uma função JScript opcional que pode ser chamada.                                                                                           |
| [Tipo de ação personalizada 54](custom-action-type-54.md) Texto VBScript especificado por um valor de propriedade.<br/>                                          | 54   | Nome da propriedade ou chave para a tabela de [Propriedades](property-table.md) .                                                                       | Uma função VBScript opcional que pode ser chamada.                                                                                          |



 

Além disso, os seguintes tipos de ação personalizada são usados com instalações simultâneas:

-   [Tipo de ação personalizada 7](custom-action-type-7.md)
-   [Tipo de ação personalizada 23](custom-action-type-23.md)
-   [Tipo de ação personalizada 39](custom-action-type-39.md)

 

 




