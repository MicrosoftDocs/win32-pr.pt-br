---
description: Este exemplo permite que o consumidor do módulo configure de forma independente um controle de edição, o atributo checksum e o atributo compactado.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Exemplo de componente configurável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768476"
---
# <a name="configurable-component-example"></a>Exemplo de componente configurável

Neste exemplo, as tabelas ModuleConfiguration e ModuleSubstitution a seguir permitem que o consumidor do módulo configure o atributo de senha de forma independente para um controle de edição, o atributo checksum de um arquivo e o atributo compactado para o mesmo arquivo.

[Tabela ModuleSubstitution](modulesubstitution-table.md)



| Tabela   | Linha           | Coluna     | Valor                        |
|---------|---------------|------------|------------------------------|
| Control | Dialog1; Edit1 | Atributos | \[= Senha\]                |
| Arquivo    | Arquivo1         | Atributos | \[= Soma de verificação \] \[ = compactado\] |



 

[Tabela ModuleConfiguration](moduleconfiguration-table.md)



| Nome       | Formatar   | Tipo | ContextData                              | DefaultValue | Atributos | DisplayName | Descrição |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Senha   | Indevida |      | 2097152; True = 2097152; Falso = 0             | 0            | 0          |             |             |
| Checksum (soma de verificação)   | Indevida |      | 1024; Soma de verificação = 1024; Nenhuma soma de verificação = 0         | 0            | 0          |             |             |
| Compressed | Indevida |      | 24576; Compactado = 16384; Não compactado = 8192 | 8192         | 0          |             |             |



 

 

 



