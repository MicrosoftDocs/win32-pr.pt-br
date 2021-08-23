---
description: ICE07 valida que o pacote de instalação especifica que as fontes sejam instaladas no FontsFolder. Se uma fonte estiver instalada em uma pasta diferente de FontsFolder, o instalador criará um atalho em vez de realmente instalar a fonte.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a0e555a35c7d5735abe0b14520d000bfeea8c888488ce37b15a78674ff9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581286"
---
# <a name="ice07"></a>ICE07

ICE07 valida que o pacote de instalação especifica que as fontes sejam instaladas no FontsFolder. Se uma fonte estiver instalada em uma pasta diferente de FontsFolder, o instalador criará um atalho em vez de realmente instalar a fonte.

A ação personalizada ICE07 faz o seguinte para cada fonte na [tabela Fonte](font-table.md).

1.  Localiza o arquivo de fonte ao qual cada título de fonte pertence usando a [tabela Fonte](font-table.md).
2.  Consulta a coluna \_ Componente da tabela Arquivo [para](file-table.md) o componente que controla cada arquivo.
3.  Consulta a coluna \_ Diretório da tabela [Componente](component-table.md) para obter uma chave na tabela Diretório.
4.  Resolve a [tabela Diretório para](directory-table.md) determinar o nome da pasta na qual o instalador deve instalar o arquivo de fonte
5.  Postará um erro se o arquivo de fonte estiver sendo instalado em uma pasta diferente de FontsFolder.

## <a name="result"></a>Resultado

ICE07 postará um erro se descobrir que o banco de dados especifica que um arquivo de fonte será instalado em uma pasta diferente de FontsFolder.

## <a name="example"></a>Exemplo

IC07 postaria a seguinte mensagem de erro para o exemplo mostrado.

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
| Myrtle | Myrtle \_ Beach |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente     | Diretório\_ |
|---------------|-------------|
| Myrtle \_ Beach | Areia     |



 

Neste exemplo, a fonte Tahoma mapeia para o arquivo de fonte Myrtle. O arquivo Myrtle pertence ao componente Myrtle \_ Beach. A resolução da tabela Diretório mostra que todos os arquivos pertencentes a Myrtle Beach devem ser \_ instalados na pasta Barra Des sandbar. Como essa não é a FontsFolder, o ICE07 posta uma mensagem de erro.

Observe que, se o componente Myrtle Beach realmente pertencer à pasta Sandbar e não ao FontsFolder, a fonte Tomaoma poderá não pertencer \_ à Myrtle \_ Beach. Uma possível correção para o erro seria incluir tahoma em outro componente que é instalado no diretório FontsFolder.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



