---
description: Uma ação personalizada pode chamar funções que são gravadas em VBScript ou JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760830"
---
# <a name="scripts"></a>Scripts

Uma ação personalizada pode chamar funções que são gravadas em VBScript ou JScript. Windows Installer não fornece o mecanismo de script. Os autores que desejam usar uma linguagem de script durante a instalação devem, portanto, garantir que o mecanismo de script apropriado esteja disponível.

O instalador não oferece suporte a JScript versão 1,0.

Uma ação personalizada de 64 bits baseada em scripts deve ser explicitamente marcada como uma ação personalizada de 64 bits, adicionando o bit **msidbCustomActionType64BitScript** ao tipo numérico Actions personalizado na coluna Type da tabela [CustomAction](customaction-table.md) . Para obter informações [, consulte ações personalizadas de 64 bits](64-bit-custom-actions.md).

Os seguintes tipos de ação personalizada básica chamam funções escritas em script.



| Tipo de ação personalizada                                 | Descrição                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Tipo de ação personalizada 5](custom-action-type-5.md)   | Arquivo JScript armazenado em um fluxo de tabela binária.                                                  |
| [Tipo de ação personalizada 21](custom-action-type-21.md) | Arquivo JScript instalado com um produto.                                                 |
| [Tipo de ação personalizada 53](custom-action-type-53.md) | Texto JScript especificado por um valor de propriedade.                                                    |
| [Tipo de ação personalizada 37](custom-action-type-37.md) | Texto JScript armazenado na coluna de destino da tabela [CustomAction](customaction-table.md) .  |
| [Tipo de ação personalizada 6](custom-action-type-6.md)   | Arquivo VBScript armazenado em um fluxo de tabela [binária](binary-table.md) .                             |
| [Tipo de ação personalizada 22](custom-action-type-22.md) | Arquivo VBScript instalado com um produto.                                                |
| [Tipo de ação personalizada 54](custom-action-type-54.md) | Texto VBScript especificado por um valor de propriedade.                                                   |
| [Tipo de ação personalizada 38](custom-action-type-38.md) | Texto VBScript armazenado na coluna de destino da tabela [CustomAction](customaction-table.md) . |



 

> [!Note]  
> O instalador executa ações personalizadas de script diretamente e não usa o Windows Script Host. O objeto **WScript** não pode ser usado dentro de uma ação personalizada de script porque esse objeto é fornecido pelo Windows Script Host. Os objetos no modelo de objeto do Windows Script Host só poderão ser usados em ações personalizadas se o Windows Script Host estiver instalado no computador criando novas instâncias do objeto, com uma chamada para CreateObject e fornecendo o ProgId do objeto (por exemplo, "WScript. Shell"). Dependendo do tipo de ação personalizada do script, o acesso a alguns objetos e métodos do modelo de objeto do Windows Script Host pode ser negado por motivos de segurança.

 

Para obter mais informações, consulte [Resumo da lista de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md) para obter um resumo de todos os tipos de ações personalizadas e como eles são codificados na tabela [CustomAction](customaction-table.md) .

 

 



