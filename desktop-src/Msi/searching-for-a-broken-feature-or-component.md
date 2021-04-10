---
description: O instalador pode aumentar a resiliência do aplicativo reinstalando automaticamente os componentes danificados.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Pesquisando um componente ou recurso desfeito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170049"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Pesquisando um componente ou recurso desfeito

O instalador pode aumentar a [resiliência](resiliency.md) do aplicativo reinstalando automaticamente os componentes danificados. Especificamente, o instalador reinstalará um componente ou recurso se descobrir que o arquivo ou a chave do registro especificado na coluna KeyPath da [tabela de componentes](component-table.md) está ausente.

Se o caminho-fonte do componente de um recurso estiver danificado na origem ou se houver um erro em como o caminho keyé criado no banco de dados, o instalador poderá tentar abrir um pacote de instalação e reinstalar o recurso sempre que o atalho do recurso for ativado.

Para determinar a causa de tentativas repetidas de reinstalar um recurso ou aplicativo, verifique o log de eventos em busca de duas entradas, como as seguintes.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

A primeira mensagem informa qual componente no pacote do produto foi instalado. Esse é o componente referenciado na \_ coluna componente da [tabela de atalho](shortcut-table.md).

A segunda mensagem informa qual componente está falhando na detecção. Esse é o componente com o caminho keyausente ou danificado que está disparando a reinstalação.

 

 



