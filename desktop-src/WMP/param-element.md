---
title: Elemento PARAM (SDK do WMP)
description: O elemento PARAM define um parâmetro personalizado associado a uma playlist ou a um elemento de uma playlist.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Elemento PARAM Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811442"
---
# <a name="param-element"></a>Elemento PARAM

O elemento **param** define um parâmetro personalizado associado a uma playlist ou a um elemento de uma playlist.

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a>Parâmetros

Um parâmetro também pode ser associado a show em vez de um clipe individual, colocando esse elemento diretamente após a tag **ASX** . Esses itens são referenciados por seus nomes e um valor de índice que começa com zero.

> [!Note]  
> Este elemento **ASX** só está disponível para o Windows Media Player versão 6, 1 e posterior. A instalação padrão do Microsoft Internet Explorer 5 inclui uma versão compatível do Windows Media Player.

 

## <a name="attributes"></a>Atributos

**NOME**

Nome usado para acessar o valor do parâmetro. O nome pode ser qualquer cadeia de caracteres válida. As cadeias de caracteres a seguir já foram definidas.



| String                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowShuffle                    | O atributo **Value** especifica se a lista de reprodução de metarquivo permite que o recurso de ordem aleatória do Windows Media Player reproduza as entradas em ordem aleatória. O atributo **Value** pode ser definido como "Yes" ou "no". O valor padrão é "no".                                                                                                                                                                                                                                                                                                                                                                  |
| Canusar                        | O atributo **Value** especifica se o usuário pode pausar a reprodução. O atributo **Value** pode ser definido como "Yes" ou "no". O valor padrão é "Sim".                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CanSeek                         | O atributo **Value** especifica se o usuário pode alterar a posição de reprodução atual usando a barra de busca, o avanço rápido ou a inversa rápida. O atributo **Value** pode ser definido como "Yes" ou "no". O valor padrão é "Sim".                                                                                                                                                                                                                                                                                                                                                                    |
| CanSkipBack                     | O atributo **Value** especifica se o usuário pode pular para o item de playlist anterior clicando em **anterior**. O atributo **Value** pode ser definido como "Yes" ou "no". O valor padrão é "Sim".                                                                                                                                                                                                                                                                                                                                                                                         |
| CanSkipForward                  | O atributo **Value** especifica se o usuário pode pular para o próximo item da playlist clicando em **Avançar**. O atributo **Value** pode ser definido como "Yes" ou "no". O valor padrão é "Sim".                                                                                                                                                                                                                                                                                                                                                                                                  |
| CPRadioID                       | O atributo **Value** especifica a ID de um feed de rádio fornecido por um repositório online tipo 1. Ou seja, o atributo **Value** deve ser igual ao campo radioid de um dos feeds de rádio no catálogo da loja online. O elemento pai é o elemento **ASX** .                                                                                                                                                                                                                                                                                                                                   |
| Codificação                        | O atributo **Value** é definido como "UTF-8" para indicar que o metarquivo é um arquivo codificado Unicode (UTF-8).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| HtmlFlink                       | O atributo **Value** é uma cadeia de caracteres fornecida por um repositório online tipo 1. O Windows Media Player passa a cadeia de caracteres para o método [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , que é implementado pelo plug-in da loja online. O método **GetItemInfo** retorna a URL da página da Web a ser exibida no painel em **execução** do Player. A página da Web tem acesso a todos os métodos que o objeto **externo** expõe para armazenamentos do tipo 1. Para obter uma lista desses métodos, consulte [external Object for tipo 1 online Stores](external-object-for-type-1-online-stores.md). |
| HTMLView                        | O atributo **Value** especifica uma URL que é exibida no painel em **execução** do player de modo completo pela duração da lista de reprodução ou da entrada atual, dependendo se o elemento pai é o elemento **ASX** ou um elemento de **entrada** . HTMLView não tem suporte para o controle do Windows Media Player.                                                                                                                                                                                                                                                                               |
| Log:*FieldName* \[ :*namespace*\] | O atributo **Value** especifica o valor para o qual o campo de log indicado será definido. A parte:*namespace* do atributo **Name** é opcional.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Antes do buffer                       | O atributo **Value** especifica se a próxima entrada da playlist começa a ser armazenada em buffer antes do final da entrada atual, o que permite uma transição direta. O atributo **Value** pode ser definido como "true" ou "false".                                                                                                                                                                                                                                                                                                                                                                                 |
| ShowWhileBuffering              | O atributo **Value** especifica se um arquivo de imagem referenciado pelo elemento de **entrada** atual continua a ser exibido após o tempo de duração especificado, enquanto a próxima entrada de playlist é armazenada em buffer. O atributo **Value** pode ser definido como "true" ou "false".                                                                                                                                                                                                                                                                                                                                         |



 

**VALUE**

Valor associado a esse parâmetro. Pode ser um valor numérico ou de cadeia de caracteres.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos           |
|-----------------|--------------------|
| Elementos pai | **ASX**, **entrada** |
| Elementos filho  | Nenhum               |



 

## <a name="remarks"></a>Comentários

Esse elemento permite que os usuários coloquem informações adicionais sobre cada clipe dentro do elemento de **entrada** que o contém. Para recuperar as informações de metadados especificadas na **entrada** da playlist, use a *mídia*. método **getItemInfo** . A *mídia*. o método **getItemInfo** recupera o valor do atributo **Value** , dado o nome do parâmetro. As versões anteriores do Windows Media Player recuperam as informações de metadados especificadas na **entrada** da playlist, usando o método **GetMediaParameter** , dado o nome do parâmetro e um número de índice para a entrada.

Um parâmetro também pode ser associado a show em vez de um clipe individual, colocando esse elemento diretamente após a tag **ASX** . Esses itens são referenciados por seus nomes e um valor de índice que começa com zero.

**Observação**

Este elemento **ASX** só está disponível para o Windows Media Player versão 6, 1 e posterior. A instalação padrão do Microsoft Internet Explorer 5 inclui uma versão compatível do Windows Media Player.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | O Windows Media Player versão 7,0 ou posterior, o Windows Media Player 9 Series ou posterior é necessário para os atributos de nome predefinidos, o Windows Media Player 10 ou posterior é necessário para os nomes predefinidos CanPause, CanSeek, CanSkipBack e CanSkipForward<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Log de dados de fluxo**](logging-stream-data.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





