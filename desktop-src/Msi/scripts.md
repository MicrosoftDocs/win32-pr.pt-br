---
description: Uma ação personalizada pode chamar funções que são escritas em VBScript ou JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Scripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af49e1863d43956e8ec799e467d8391873458d1879f78455abda9ee06fb739aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041366"
---
# <a name="scripts"></a>Scripts

Uma ação personalizada pode chamar funções que são escritas em VBScript ou JScript. Windows O instalador não fornece o mecanismo de script. Os autores que desejam usar uma linguagem de script durante a instalação devem, portanto, garantir que o mecanismo de script apropriado está disponível.

O instalador não dá suporte JScript versão 1.0.

Uma ação personalizada de 64 bits baseada em scripts deve ser marcada explicitamente como uma ação personalizada de 64 bits adicionando o bit **msidbCustomActionType64BitScript** ao tipo numérico ações personalizadas na coluna Tipo da tabela [CustomAction.](customaction-table.md) Para obter informações, [consulte Ações personalizadas de 64 bits.](64-bit-custom-actions.md)

Os seguintes tipos de ação personalizados básicos chamam funções escritas no script.



| Tipo de ação personalizado                                 | Descrição                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Tipo de ação personalizada 5](custom-action-type-5.md)   | JScript arquivo armazenado em um fluxo de tabela binário.                                                  |
| [Tipo de ação personalizada 21](custom-action-type-21.md) | JScript arquivo instalado com um produto.                                                 |
| [Tipo de ação personalizada 53](custom-action-type-53.md) | JScript texto especificado por um valor de propriedade.                                                    |
| [Tipo de ação personalizada 37](custom-action-type-37.md) | JScript texto armazenado na coluna Destino da [tabela CustomAction.](customaction-table.md)  |
| [Tipo de ação personalizada 6](custom-action-type-6.md)   | Arquivo VBScript armazenado em um [fluxo de tabela](binary-table.md) binário.                             |
| [Tipo de ação personalizada 22](custom-action-type-22.md) | Arquivo VBScript instalado com um produto.                                                |
| [Tipo de ação personalizada 54](custom-action-type-54.md) | Texto do VBScript especificado por um valor de propriedade.                                                   |
| [Tipo de ação personalizada 38](custom-action-type-38.md) | Texto VBScript armazenado na coluna Destino da [tabela CustomAction.](customaction-table.md) |



 

> [!Note]  
> O instalador executa ações personalizadas de script diretamente e não usa o host Windows Script. O **objeto WScript** não pode ser usado dentro de uma ação personalizada de script porque esse objeto é fornecido pelo host Windows Script. Os objetos no modelo de objeto Host de Script do Windows só poderão ser usados em ações personalizadas se o Host de Script do Windows estiver instalado no computador criando novas instâncias do objeto, com uma chamada para CreateObject e fornecendo a ProgId do objeto (por exemplo, "WScript.Shell"). Dependendo do tipo de ação personalizada de script, o acesso a alguns objetos e métodos do modelo de objeto Windows Host de Script pode ser negado por motivos de segurança.

 

Para obter mais informações, consulte [Lista](summary-list-of-all-custom-action-types.md) resumida de todos os tipos de ação personalizados para obter um resumo de todos os tipos de ações personalizadas e como eles são codificados na [tabela CustomAction.](customaction-table.md)

 

 



