---
description: ICE07 valida que o pacote de instalação especifica que as fontes sejam instaladas no FontsFolder. Se uma fonte for instalada em uma pasta que não seja a FontsFolder, o instalador criará um atalho em vez de realmente instalar a fonte.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750004"
---
# <a name="ice07"></a>ICE07

ICE07 valida que o pacote de instalação especifica que as fontes sejam instaladas no FontsFolder. Se uma fonte for instalada em uma pasta que não seja a FontsFolder, o instalador criará um atalho em vez de realmente instalar a fonte.

A ação personalizada ICE07 faz o seguinte para cada fonte na [tabela de fontes](font-table.md).

1.  Localiza o arquivo de fonte ao qual o título de cada fonte pertence usando a [tabela de fontes](font-table.md).
2.  Consulta a \_ coluna componente da [tabela de arquivos](file-table.md) do componente que controla cada arquivo.
3.  Consulta a \_ coluna Directory da [tabela de componentes](component-table.md) para obter uma chave na tabela de diretórios.
4.  Resolve a tabela de [diretórios](directory-table.md) para determinar o nome da pasta na qual o instalador deve instalar o arquivo de fonte
5.  Posta um erro se o arquivo de fonte está sendo instalado em uma pasta que não seja a FontsFolder.

## <a name="result"></a>Resultado

ICE07 posta um erro se descobrir que o banco de dados especifica que um arquivo de fonte seja instalado em uma pasta que não seja a FontsFolder.

## <a name="example"></a>Exemplo

IC07 publicaria a seguinte mensagem de erro para o exemplo mostrado.

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[Tabela de fontes](font-table.md)



| Arquivo\_ | FontTitle |
|--------|-----------|
| Myrtle | Tahoma    |



 

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo   | Componente\_   |
|--------|---------------|
| Myrtle | \_Praia Myrtle |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente     | Diretório\_ |
|---------------|-------------|
| \_Praia Myrtle | SandBar     |



 

Neste exemplo, a fonte Tahoma é mapeada para o arquivo de fonte Myrtle. O arquivo Myrtle pertence ao componente Myrtle \_ praia. A resolução da tabela de diretórios mostra que todos os arquivos pertencentes à \_ praia Myrtle devem ser instalados na pasta Sandbar. Como esse não é o FontsFolder, o ICE07 posta uma mensagem de erro.

Observe que, se o componente Myrtle da \_ praia realmente pertence à pasta Sandbar, e não ao FontsFolder, a fonte Tahoma pode não pertencer a Myrtle \_ praia. Uma possível correção para o erro seria incluir Tahoma em outro componente que é instalado no diretório FontsFolder

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



