---
description: ICE26 valida as tabelas de sequência em um banco de dados Windows Installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf63e0efeec79de35122f7a210c32746af9de50f27ac3e47ad1f88984a6ec77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528856"
---
# <a name="ice26"></a>ICE26

ICE26 valida que cada uma das tabelas de [*sequência*](s-gly.md) a seguir contém as ações exigidas pela tabela e não contém nenhuma ação não permitida na tabela:

-   [Tabela AdminUISequence](adminuisequence-table.md)
-   [Tabela AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabela InstallUISequence](installuisequence-table.md)
-   [Tabela InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE26 posta uma mensagem de erro se o pacote de instalação tiver uma tabela de sequência que não tem uma ação necessária ou que contenha uma ação que não é permitida para a tabela.

## <a name="example"></a>Exemplo



| Erro de ICE26                                                                   | Descrição                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ação: ' Action1 ' é necessário na tabela de sequência InstallExecuteSequence.   | Uma ação necessária está ausente na tabela de sequência indicada. Consulte a template.msi ou as tabelas de sequência sugeridas em [usando uma tabela de sequência](using-a-sequence-table.md). |
| Ação: ' Action2 ' é proibido na tabela de sequência InstallExecuteSequence. | Esta ação não pode estar na tabela de sequência indicada. Remova esta ação da tabela de sequência.                                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



