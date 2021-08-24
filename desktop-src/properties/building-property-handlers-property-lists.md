---
description: Depois de avaliar sua estratégia de propriedade, você deve determinar quais propriedades mostrar na interface do usuário Windows Explorer e onde.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Usando listas de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72289612d61ebfb198ec0f2ee3d4a7d206209e91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477392"
---
# <a name="using-property-lists"></a>Usando listas de propriedades

Depois de avaliar sua estratégia de propriedade, você deve determinar quais propriedades mostrar na interface do usuário Windows Explorer e onde. Há vários locais em que as propriedades são exibidas de maneira somente leitura. A edição de propriedade, por outro lado, está habilitada somente na **caixa de diálogo** Propriedades. Essa caixa de diálogo pode ser invocada  por meio do link **Editar Propriedades** no Painel de Visualização ou no menu de atalho de um item.

As listas de propriedades são cadeias de caracteres delimitadas por pontos e vírgulas que têm o formulário a seguir.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



O único sinalizador disponível no momento é mostrado na tabela a seguir.



| Sinalizador | Descrição                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | Não mostre a propriedade no Painel **de Visualização,** conforme instruído no valor da chave do Registro **PreviewDetails.** Veja o exemplo que segue a tabela a seguir se o valor da propriedade não estiver definido. |



 

Depois de definir uma lista de propriedades, você pode armazenar essa cadeia de caracteres no Registro por meio do sistema de associação de arquivos [shell](../shell/fa-file-types.md) padrão em **HKEY \_ CLASSES \_ ROOT.** A tabela a seguir resume os valores das listas de propriedades que podem ser atribuídos na chave do Registro para uma extensão de nome de arquivo específica.




| Valor | Descrição | 
|-------|-------------|
| FullDetails | As propriedades são exibidas na <strong>guia Detalhes</strong> da caixa <strong>de diálogo</strong> Propriedades . Esta é a lista completa de propriedades às qual o tipo de arquivo dá suporte. | 
| PreviewDetails | As propriedades são exibidas no <strong>Painel de Visualização</strong>. | 
| PreviewTitle | As propriedades são exibidas na área de título do <strong>Painel</strong> de Visualização ao lado da miniatura do item. O número máximo de entradas é 3. Se a lista de propriedades contiver mais do que o número máximo permitida, o restante das entradas será ignorado. | 
| TileInfo | As propriedades são exibidas quando a exibição de lista está no <strong>modo de exibição Blocos.</strong> O número máximo de entradas é 3. Se a lista de propriedades contiver mais do que o número máximo permitida, o restante das entradas será ignorado.<blockquote>[!Note]<br />Esse valor estava presente no Windows XP.</blockquote><br /> | 
| ExtendedTileInfo | As propriedades são exibidas para um item quando a exibição de lista está no <strong>modo de exibição de Peça</strong> Estendida. | 
| InfoTip | As propriedades são exibidas em uma infotip quando um usuário passar o mouse sobre um item.<blockquote>[!Note]<br />Esse valor estava presente no Windows XP.</blockquote><br /> | 
| Quicktip | As propriedades são exibidas quando é difícil recuperar propriedades diretamente de um item, como quando o item deve ser acessado por uma conexão de rede lenta. É recomendável que as propriedades nomeadas aqui, como Tipo ou Tamanho, não exigem a abertura do fluxo de arquivos para determinar seu valor.<blockquote>[!Note]<br />Esse valor estava presente no Windows XP.</blockquote><br /> | 




 

O exemplo a seguir define o valor PreviewDetails para um tipo de arquivo .recipe, usando um ProgID de **RecipeKey**.

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Conforme explicado no tópico [associação de arquivo shell,](../shell/fa-file-types.md) associações de arquivos podem ser descritas para o formulário mais específico para o formulário mais geral. O formulário mais específico é a extensão de nome de arquivo único e o formulário mais genérico é uma chave que se aplica a todos os arquivos e pastas de arquivos. Entre esses dois extremos, você também pode definir um [PROGID](../shell/fa-progids.md) que agrupa um conjunto de extensões de nome de arquivo (por exemplo, tipos .jpg e .jpeg agrupados como **jpegfile**). Ao definir listas de propriedades, você deve defini-las para ProgIDs ou, em alguns casos, extensões de nome de arquivo específicas. Evite depender de entradas amplas, como a **chave AllFileSystemObjects.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
</dt> <dt>

[Usando nomes de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Inicializando manipuladores de propriedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
