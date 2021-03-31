---
description: Depois de avaliar sua estratégia de propriedade, você deve determinar quais propriedades mostrar na interface do usuário do Windows Explorer e onde.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Usando listas de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8644e0d51141751ac55d50966cd6163a3359435d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921343"
---
# <a name="using-property-lists"></a>Usando listas de propriedades

Depois de avaliar sua estratégia de propriedade, você deve determinar quais propriedades mostrar na interface do usuário do Windows Explorer e onde. Há vários locais onde as propriedades são exibidas em uma maneira somente leitura. A edição de propriedade, por outro lado, é habilitada apenas na caixa de diálogo **Propriedades** . Essa caixa de diálogo pode ser chamada por meio do link **Editar propriedades** no **painel de visualização** ou do menu de atalho de um item.

As listas de propriedades são cadeias de caracteres delimitadas por ponto e vírgula que têm o seguinte formato.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



O único sinalizador disponível no momento é mostrado na tabela a seguir.



| Sinalizador | Descrição                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | Não mostre a propriedade no painel de **Visualização** conforme instruído no valor da chave do registro **PreviewDetails** . Consulte o exemplo que segue a próxima tabela se o valor da propriedade não estiver definido. |



 

Depois de definir uma lista de propriedades, você pode armazenar essa cadeia de caracteres no registro por meio do sistema de [Associação de arquivo do Shell](../shell/fa-file-types.md) padrão sob a raiz de **\_ classes hKey \_ .** A tabela a seguir resume os valores para as listas de propriedades que podem ser atribuídas na chave do registro para uma extensão de nome de arquivo específica.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FullDetails</td>
<td>As propriedades são exibidas na guia <strong>detalhes</strong> da caixa de diálogo <strong>Propriedades</strong> . Esta é a lista completa de propriedades às quais o tipo de arquivo dá suporte.</td>
</tr>
<tr class="even">
<td>PreviewDetails</td>
<td>As propriedades são exibidas no <strong>painel de visualização</strong>.</td>
</tr>
<tr class="odd">
<td>PreviewTitle</td>
<td>As propriedades são exibidas na área de título do <strong>painel de visualização</strong> ao lado da miniatura do item. O número máximo de entradas é 3. Se a lista de propriedades contiver mais do que o número máximo permitido, o restante das entradas será ignorado.</td>
</tr>
<tr class="even">
<td>TileInfo</td>
<td>As propriedades são exibidas quando o modo de exibição de lista está no modo de exibição de <strong>blocos</strong> . O número máximo de entradas é 3. Se a lista de propriedades contiver mais do que o número máximo permitido, o restante das entradas será ignorado.
<blockquote>
[!Note]<br />
Esse valor estava presente no Windows XP.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>ExtendedTileInfo</td>
<td>As propriedades são exibidas para um item quando o modo de exibição de lista está no modo de exibição de <strong>bloco estendido</strong> .</td>
</tr>
<tr class="even">
<td>InfoTip</td>
<td>As propriedades são exibidas em uma InfoTip quando um usuário passa o mouse sobre um item.
<blockquote>
[!Note]<br />
Esse valor estava presente no Windows XP.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>QuickTip</td>
<td>As propriedades são exibidas quando é difícil recuperar as propriedades diretamente de um item, como quando o item deve ser acessado por uma conexão de rede lenta. É recomendável que as propriedades nomeadas aqui, como tipo ou tamanho, não exijam a abertura do fluxo de arquivos para determinar seu valor.
<blockquote>
[!Note]<br />
Esse valor estava presente no Windows XP.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

O exemplo a seguir define o valor de PreviewDetails para um tipo de arquivo. Recipe, usando um ProgID de **RecipeKey**.

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Conforme explicado no tópico [Associação de arquivo do Shell](../shell/fa-file-types.md) , as associações de arquivo podem ser descritas para o mais específico para a forma mais geral. A forma mais específica é a extensão de nome de arquivo único e a forma mais genérica é uma chave que se aplica a todos os arquivos e pastas de arquivos. Entre esses dois extremos, você também pode definir um [ProgID](../shell/fa-progids.md) que agrupa um conjunto de extensões de nome de arquivo (por exemplo, os tipos. jpg e. jpeg agrupados como **jpegfile**). Ao definir listas de propriedades, você deve defini-las para ProgIDs ou, em alguns casos, extensões de nome de arquivo específicas. Evite depender de entradas amplas, como a chave **AllFileSystemObjects** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
</dt> <dt>

[Usando nomes de tipos](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
