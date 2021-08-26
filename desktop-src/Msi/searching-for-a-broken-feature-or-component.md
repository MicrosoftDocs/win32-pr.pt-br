---
description: O instalador pode aumentar a resiliência do aplicativo reinstalando automaticamente os componentes danificados.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Procurando um recurso ou componente desfeito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa17fc66fdf0bda0a04df9a5917d4e79671b32f453ead921d4f43f89bbd47dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041236"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Procurando um recurso ou componente desfeito

O instalador pode aumentar [a resiliência do aplicativo](resiliency.md) reinstalando automaticamente os componentes danificados. Especificamente, o instalador reinstala um componente ou recurso se descobrir que o arquivo ou a chave do Registro especificado na coluna KeyPath da tabela [Component](component-table.md) está ausente.

Se o KeyPath do componente de um recurso estiver danificado na origem ou se houver um erro em como o KeyPath é autor no banco de dados, o instalador poderá tentar abrir um pacote de instalação e reinstalar o recurso sempre que o atalho do recurso for ativado.

Para determinar a causa de tentativas repetidas de reinstalar um recurso ou aplicativo, verifique o Log de Eventos em busca de duas entradas, como a seguir.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

A primeira mensagem informa qual componente no pacote do produto estava sendo instalado. Esse é o componente referenciado na coluna \_ Componente da tabela [Atalho](shortcut-table.md).

A segunda mensagem informa qual componente está falhando na detecção. Esse é o componente com o KeyPath ausente ou danificado que está disparando a reinstalação.

 

 



