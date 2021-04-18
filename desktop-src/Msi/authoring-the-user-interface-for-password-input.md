---
description: Para cada senha que deve ser inserida pelo usuário, adicione um controle de edição em uma caixa de diálogo que armazena o valor da senha em uma propriedade.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Criando a interface do usuário para entrada de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753454"
---
# <a name="authoring-the-user-interface-for-password-input"></a>Criando a interface do usuário para entrada de senha

Para cada senha que deve ser inserida pelo usuário, adicione um controle de edição em uma caixa de diálogo que armazena o valor da senha em uma propriedade. Esse [controle de edição](edit-control.md) deve ter o [atributo de controle de senha](password-control-attribute.md). Isso especifica que a propriedade inserida é uma senha e impede que o instalador grave a propriedade no arquivo de log.

Os [atributos de controle](control-attributes.md) para o controle de edição de senha são MsidbControlAttributesVisible, MsidbControlAttributesEnabled e msidbControlAttributesPasswordInput (1 + 2 + 2097152). O X, Y, largura, altura e controle, \_ em seguida, dependem do layout do controle na caixa de diálogo.

[Tabela de controle](control-table.md)



| caixa de diálogo\_ | controle\_            | Type | X   | S   | Largura | Altura | Atributos | Propriedade         | Texto | \_Próximo controle | Ajuda |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| MyDialog | TestUserPasswordEdit | Editar | 25  | 120 | 300   | 20     | 2097155    | TESTUSERPASSWORD |      | Cancelar        |      |



 

Continue a [proteger a instalação](securing-the-installation.md).

 

 



