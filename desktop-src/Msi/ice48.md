---
description: O ICE48 verifica os diretórios que são embutidos em código para caminhos locais na tabela de propriedades.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787500"
---
# <a name="ice48"></a>ICE48

O ICE48 verifica os diretórios que são embutidos em código para caminhos locais na [tabela de propriedades](property-table.md).

Não codifique caminhos de diretório para unidades locais porque computadores diferem na configuração da unidade local. Essa prática pode ser aceitável se estiver implantando um aplicativo em um grande número de computadores nos quais as partes relevantes das unidades são todas iguais.

## <a name="result"></a>Resultado

ICE48 posta uma mensagem de erro se houver um diretório embutido em código para um caminho local na tabela de propriedades.

## <a name="example"></a>Exemplo

ICE48 relataria o seguinte aviso para o exemplo mostrado.

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

[Tabela de diretórios](directory-table.md) (parcial)



| Diretório | Pai do diretório \_ | DefaultDir |
|-----------|-------------------|------------|
| Dir1      |                   | SourceDir  |



 

[Tabela de propriedades](property-table.md) (parcial)



| Propriedade | Valor      |
|----------|------------|
| Dir1     | d: \\ origem |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



