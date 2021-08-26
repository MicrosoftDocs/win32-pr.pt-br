---
title: Elemento fragment
description: O elemento fragment especifica uma condição da consulta que seleciona itens da biblioteca. As condições são especificadas por cadeias de caracteres de condição. Uma cadeia de caracteres de condição normalmente tem uma parte de nome, uma parte de condição e uma parte de valor.
ms.assetid: 1575318f-8527-42ba-9c2f-9993a60987d7
keywords:
- elemento fragment Windows Media Player
topic_type:
- apiref
api_name:
- fragment Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1010b269302f88f163232bcaf3e37111e5fc219944ff1d141c1189e119bba05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003696"
---
# <a name="fragment-element"></a>Elemento fragment

O **elemento** fragment especifica uma condição da consulta que seleciona itens da biblioteca. As condições são especificadas por cadeias de caracteres de condição. Uma cadeia de caracteres de condição normalmente tem uma parte de nome, uma parte de condição e uma parte de valor.

``` syntax
<fragment
    name = "string"
>
</fragment>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obrigatório) 
</dt> <dd>

Uma parte de uma cadeia de caracteres de condição. Consulte Observações.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia | Elementos                                                               |
|-----------|------------------------------------------------------------------------|
| Pai    | [filter](filter-element.md), [sourceFilter](sourcefilter-element.md) |
| Filho     | [argument](argument-element.md)                                       |



 

## <a name="remarks"></a>Comentários

Determinadas cadeias de caracteres de condição têm uma parte de atributo de metadados, uma parte de condição e uma parte de valor. Por exemplo, na cadeia de caracteres de condição "Album Artist Is Joe", a parte do atributo de metadados é "Album Artist", a parte da condição é "Is" e a parte do valor é "Joe".

Exemplo:


```XML
<fragment name = "Album Artist">
    <argument name = "condition">Is</argument>
    <argument name = "value">Joe</argument>
</fragment>
```



Para cadeias de caracteres de condição desse tipo, a tabela a seguir mostra os possíveis atributos de metadados, as possíveis condições e os valores possíveis:



| Atributo de metadados                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Condições possíveis                                                                                             | Valores possíveis                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AtorAlbum Artist<br/> Título do álbum<br/> Autor<br/> Legenda<br/> Canal<br/> Compositor<br/> Condutor<br/> Provedor de Conteúdo<br/> Gênero do provedor de conteúdo<br/> Artista colaborador<br/> Texto de direitos autorais<br/> Diretor<br/> Episódio<br/> Tipo de arquivo<br/> Gênero<br/> Chave<br/> Palavras-chave<br/> Idioma<br/> Humor<br/> Classificação dos pais<br/> Período<br/> Produtor<br/> Provedor<br/> Publisher<br/> Série<br/> Nome da estação<br/> Subgênero<br/> Subtítulo<br/> Título<br/> Gravador<br/> | EqualsDoes não é igual a<br/> É<br/> Não é<br/> Contém<br/> Não contém<br/> | Qualquer valor de cadeia de caracteres                                                                                                                                                                                                                                                                                                  |
| Taxa de bits (em quilobytes por segundo.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | EqualsDoes não é igual a<br/> É<br/> Não é<br/> Contém<br/> Não contém<br/> | 4864<br/> 96<br/> 128<br/> 160<br/> 192<br/> 256<br/> 300<br/> 500<br/> 750<br/> 1000<br/> 1500<br/> 3000<br/> 4500<br/> 6000<br/> 7500<br/>                                                                            |
| Tipo de mídia secundária                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | EqualsDoes não é igual a<br/> É<br/> Não é<br/> Contém<br/> Não contém<br/> | Áudio: NewsAudio: Talk Show<br/> Áudio: Audio Books<br/> Áudio: Palavra Falada em Áudio<br/> Vídeo: Notícias<br/> Vídeo: Talk Show<br/> Vídeo: Home Video<br/> Vídeo: Filme/Filme<br/> Vídeo: programa de TV<br/> Vídeo: Vídeo corporativo<br/> Vídeo: vídeo de música<br/> |
| Altura da imagem do tamanho do arquivo (em KB)<br/> Largura da imagem<br/> Contagem de execuções: totais da tarde<br/> Contagem de execuções: totais da noite<br/> Contagem de execuções: totais da manhã<br/> Contagem de execuções: totais da noite<br/> Contagem de execuções: total geral<br/> Contagem de execuções: total da semana<br/> Contagem de execuções: total de fim de semana<br/>                                                                                                                                                                                                                                                                                                                  | É menor que o maior que<br/> É<br/> Não é<br/>                                          | Qualquer número                                                                                                                                                                                                                                                                                                        |
| Data de transmissão codificada<br/> Data de gravação<br/> Data de início<br/> Ano de lançamento<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | É antes de<br/> É<br/> Não é<br/>                                                    | YesterdayLast semana<br/> Mês passado<br/> 6 meses<br/> 1 ano<br/> 2 anos<br/> 5 anos<br/> 2000s<br/> 90<br/> anos<br/> 70<br/> anos<br/> 1950s<br/> 1940s<br/>                                                            |
| Data de adição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | É antes de<br/> É<br/> Não é<br/>                                                    | YesterdayLast semana<br/> Mês passado<br/> 6 meses<br/> 1 ano<br/> 2 anos<br/> 5 anos<br/>                                                                                                                                                                                   |
| Data da última execução                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Mais antigo ThanMore recente que<br/> É<br/> Não é<br/>                                           | YesterdayLast semana<br/> Mês passado<br/> 6 meses<br/> 1 ano<br/> 2 anos<br/> 5 anos<br/>                                                                                                                                                                                   |
| Mês de uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | É antes de mais recente do que<br/> É<br/> Não é<br/>                                         | 12<br/> 3<br/> 4<br/> 5<br/> 6<br/> 7<br/> 8<br/> 9<br/> 10<br/> 11<br/> 12<br/> 13<br/>                                                                                                                                                  |
| Ano de uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | É antes de mais recente do que<br/> É<br/> Não é<br/>                                         | Qualquer ano                                                                                                                                                                                                                                                                                                          |
| Classificação automática de RatingMy<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Pelo menos não é mais do que<br/> É<br/> Não é<br/>                                           | Unrated1 estrela<br/> 2 estrelas<br/> 3 estrelas<br/> 4 estrelas<br/> 5 estrelas<br/>                                                                                                                                                                                                              |
| Campo personalizado \# 1Custom campo \# 2<br/> Nome do Arquivo<br/> Campos de chave<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | ContainsDoes não contém<br/>                                                                             | Qualquer cadeia de caracteres                                                                                                                                                                                                                                                                                                        |



 

Determinadas cadeias de caracteres de condição têm uma parte de limite, uma parte de número e uma parte de formato. Por exemplo, na cadeia de caracteres de condição "limitar tamanho total a 3 megabytes", a parte do limitador é "limitar tamanho total", a parte de número é "3" e a parte de formato é "megabytes".

Exemplo:


```XML
<fragment name = "Limit Total Size To">
  <argument name = "number">3</argument>
  <argument name = "format">Megabytes</argument>
</fragment>
```



Para cadeias de caracteres de condição desse tipo, a tabela a seguir mostra os possíveis limites e formatos.



| Limitador                 | Números possíveis | Formatos possíveis                |
|-------------------------|------------------|---------------------------------|
| Limitar tamanho total a     | Qualquer número       | Kilobytes, megabytes, gigabytes |
| Limitar duração total a | Qualquer número       | Segundos, Minutos, Horas, Dias   |



 

Determinadas cadeias de caracteres de condição têm uma parte do limitador e uma parte de número. Por exemplo, na cadeia de caracteres de condição "Limitar Número de Itens a 25", a parte do limitador é "Número limite de itens" e a parte do número é "25".

Exemplo:


```XML
<fragment name = "Limit Number of Items">
    <argument name = "number">25</argument>
</fragment>
```



Para cadeias de caracteres de condição desse tipo, a tabela a seguir mostra o único limitador possível.



| Limitador               | Números possíveis |
|-----------------------|------------------|
| Número limite de itens | Qualquer número       |



 

Determinadas cadeias de caracteres de condição têm uma parte de proteção e uma parte de condição. Por exemplo, na cadeia de caracteres de condição "Proteção Está presente", a parte de proteção é "Proteção" e a parte da condição é "Is".

Exemplo:


```XML
<fragment name = "Protection">
    <argument name = "condition">Is</argument>
</fragment>
```



Para cadeias de caracteres de condição desse tipo, a tabela a seguir mostra as possíveis condições.



| Parte de proteção | Condições possíveis             |
|--------------------|---------------------------------|
| Proteção         | É<br/> Não é<br/> |



 

Há um tipo de elemento **de fragmento** que não contém uma cadeia de caracteres de condição. Se o atributo name de um **elemento de fragmento** for "Ordem de Reprodução Aleatória", o elemento de **fragmento** não conterá **elementos de** argumento. Esse **elemento** de fragmento instrui o jogador a reproduzir a lista em ordem aleatória.

Exemplo:


```XML
<fragment name = "Randomize Playback Order">
</fragment>
```



Determinadas cadeias de caracteres de condição têm uma parte de classificação, uma parte de valor e uma parte de condição. Por exemplo, na cadeia de caracteres de condição "Classificar por ordem crescente de título", a parte de classificação é "Classificar por", a parte do valor é "Título" e a parte da condição é "Crescente". Observe que, nesse caso, a parte do valor é um atributo de metadados.

Exemplo:


```XML
<fragment name = "Sort By">
    <argument name = "value">Title</argument>
    <argument name = "condition">Ascending</argument>
</fragment>
```



Para cadeias de caracteres de condição desse tipo, a tabela a seguir mostra os possíveis valores e condições.



| Parte de classificação | Valores possíveis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Condições possíveis                              |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Classificar Por      | GenreTitle<br/> Data de adição<br/> Classificação automática<br/> Minha Classificação<br/> Contagem de reprodução: total geral<br/> Contagem de reprodução: totais de manhã<br/> Contagem de reprodução: totais de tarde<br/> Contagem de reprodução: totais da noite<br/> Contagem de reprodução: totais de noite<br/> Contagem de reprodução: Total de dias da semana<br/> Contagem de reprodução: fim de semana total<br/> Ator<br/> Subtítulo<br/> Nome da estação<br/> Canal<br/> Hora da difusão<br/> Diretor<br/> Ano de lançamento<br/> Gravador<br/> Produtor<br/> Data registrada<br/> Data codificada<br/> Taxa de bits<br/> Proteção<br/> | AscendingDescending<br/> Aleatório<br/> |



 

Ao usar um elemento de fragmento para classificar uma playlist, você deve classificar um atributo de metadados que se aplica ao tipo de itens de mídia que você está classificação. Por exemplo, se você estiver classificação de itens de música, não poderá classificar em Ator. A tabela a seguir mostra quais atributos de metadados você pode usar para classificar quais tipos de mídia.



| Típo de mídia  | Atributos de metadados possíveis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Música       | GenreTitle<br/> Data de adição<br/> Classificação automática<br/> Minha Classificação<br/> Contagem de reprodução: total geral<br/> Contagem de reprodução: totais de manhã<br/> Contagem de reprodução :Totais de tarde<br/> Contagem de reprodução :Totais da noite<br/> Contagem de reprodução :Totais de noite<br/> Contagem de reprodução :Total weekday<br/> Contagem de reprodução: fim de semana total<br/>                                                                                                                                                                                                                                                                                            |
| Vídeo ou TV | GenreActor<br/> Subtítulo<br/> Título<br/> Data de adição<br/> Classificação automática<br/> Nome da estação<br/> Canal<br/> Hora da difusão<br/> Diretor<br/> Ano de lançamento<br/> Gravador<br/> Produtor<br/> Data registrada<br/> Data codificada<br/> Taxa de bits<br/> Minha Classificação<br/> Proteção<br/> Contagem de reprodução: total geral<br/> Contagem de reprodução: totais de manhã<br/> Contagem de reprodução: totais de tarde<br/> Contagem de reprodução: totais da noite<br/> Contagem de reprodução: totais de noite<br/> Contagem de reprodução: Total de dias da semana<br/> Contagem de reprodução: fim de semana total<br/> |
| Opção       | TitleDate adicionado<br/> Taxa de bits<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Photo       | Título                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Outro       | GenreTitle<br/> Data de adição<br/> Classificação automática<br/> Minha Classificação<br/> Taxa de bits<br/> Contagem de reprodução: total geral<br/> Contagem de reprodução: totais de manhã<br/> Contagem de reprodução: totais de tarde<br/> Contagem de reprodução: totais da noite<br/> Contagem de reprodução: totais de noite<br/> Contagem de reprodução: Total de dias da semana<br/> Contagem de reprodução: fim de semana total<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento filter**](filter-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Referência de elementos da playlist de mídia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





