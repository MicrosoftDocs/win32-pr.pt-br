---
title: Aviso da tabela de dados do ARIA
description: Aviso da tabela de dados do ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006040"
---
# <a name="aria-data-table-warning"></a>Aviso da tabela de dados do ARIA

## <a name="text"></a>Texto

A tabela contém dados, mas não tem nenhum resumo nem um atributo **DescribedBy do Aria** válido.

## <a name="type"></a>Tipo

Aviso

## <a name="description"></a>Descrição

Esse aviso se aplica a tabelas HTML com mais de uma célula. Ele não se aplica a tabelas com `role="presentation"` uma vez que elas são consideradas como tabelas de layout.

Esse aviso indica que a tabela é identificada como uma tabela de dados, mas não tem uma descrição acessível definida.

> [!Note]  
> Nem todas as tabelas de dados precisam ter uma descrição acessível. Você deve definir uma descrição acessível se os usuários precisarem de mais informações para entender a estrutura e o conteúdo da tabela de dados.

 

Para resolver esse aviso, defina uma descrição acessível de tabela usando o atributo Summary ou o atributo **Aria-DescribedBy** .

## <a name="example"></a>Exemplo


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




