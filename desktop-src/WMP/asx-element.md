---
title: Elemento ASX
description: O elemento ASX define um arquivo como um metadado.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Elemento ASX Windows Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 509cdbc25c57c6d0b556433c3bee8b1e68083248c8356769a31529b83c2df1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902825"
---
# <a name="asx-element"></a>Elemento ASX

O **elemento ASX** define um arquivo como um metadado.

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a>Atributos

`VERSION` (obrigatório)

Número decimal que representa o número de versão da sintaxe para o metadado. Definido como 3 ou 3.0.

**PREVIEWMODE** (opcional)

Valor que indica se Windows Media Player entra no modo de visualização antes de tocar o primeiro clipe.

Deve ser um dos valores a seguir.



| Valor | Descrição                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | Windows Media Player entra no modo de visualização antes de tocar o primeiro clipe.                            |
| Não    | O valor padrão. Windows Media Player não entra no modo de visualização antes de tocar o primeiro clipe. |



 

**BANNERBAR** (opcional)

Valor que indica se Windows Media Player reserva espaço para um gráfico de faixa.

Deve ser um dos valores a seguir.



| Valor | Descrição                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | O valor padrão. Windows Media Player reserva espaço para a barra de faixas somente quando uma parte do conteúdo inclui uma.                       |
| FIXED | Windows Media Player reserva um espaço fixo para um gráfico de faixa para cada parte do conteúdo tocada, independentemente de haver uma faixa associada. |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai | Nenhum. O **elemento ASX** deve ser o primeiro elemento em cada metadado.                                                                                                 |
| Elementos filho  | **ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT,** **ENTRY,** **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE** |



 

## <a name="remarks"></a>Comentários

Os primeiros quatro caracteres de uma playlist de metadados devem ser "<ASX". Outros elementos definidos dentro do escopo do **elemento ASX,** como **TITLE** e **AUTHOR**, são associados às informações de show exibidas por Windows Media Player.

Por Windows Media Player, o número de versão da sintaxe é 3.0. Windows Media Player dá suporte a todas as versões anteriores da sintaxe de metadados. Os valores aceitáveis para **o atributo VERSION** incluem 3.0 e 3 (sem ponto decimal).

Se o valor do atributo **PREVIEWMODE** for YES, Windows Media Player entrará imediatamente no modo de visualização antes de tocar o primeiro clipe. Quando Windows Media Player entra no modo de visualização, ele visualiza cada clipe referenciado no metadado. O **elemento PREVIEWDURATION** determina a duração de cada versão prévia.

O **atributo BANNERBAR** define se Windows Media Player reserva espaço para um gráfico de faixa. Uma faixa é um gráfico que é exibido na área de exibição de vídeo enquanto o conteúdo da mídia está sendo exibido. (Use o **elemento BANNER** para adicionar uma faixa ao conteúdo.) Se o valor de **BANNERBAR** for FIXED, Windows Media Player reserva espaço de faixa para cada parte do conteúdo de mídia, independentemente de o conteúdo de mídia ter uma faixa. Se uma parte do conteúdo de mídia não tiver uma faixa associada a ele, o espaço reservado para um será preto. Se o valor do atributo **BANNERBAR** for AUTO, Windows Media Player reserva espaço para a faixa somente quando o conteúdo de mídia inclui um.

Se você criar um metadado com vários clipes (elementos **ENTRY** ou **ENTRYREF)** e definir o valor do atributo **BANNERBAR** como AUTO, o Windows Media Player poderá ser reesquisado para permitir espaço para um gráfico de faixa para um clipe e, em seguida, reorganizar novamente se o próximo clipe não tiver um gráfico de faixa. Se você quiser que o tamanho da janela permaneça o mesmo (exceto quando o tamanho do vídeo mudar), use o valor FIXO para o **atributo BANNERBAR.**

O espaço reservado para um gráfico de faixa tem 32 pixels de altura por 194 pixels de largura. O espaço reservado aparece abaixo de qualquer conteúdo de vídeo renderizado e 6 pixels acima da borda inferior da área de vídeo, permitindo espaço para a borda da área de vídeo de 6 pixels. O espaço reservado da faixa é centralizado horizontalmente.

Windows Media Player renderiza o gráfico começando no pixel mais à esquerda do espaço de faixa. Se o gráfico preencher todo o espaço, ele aparecerá centralizado horizontalmente. Caso contrário, haverá espaço à seguir. Observe que a largura mínima de Windows Media Player é sempre maior do que o tamanho do clipe de vídeo, independentemente do valor do **atributo BANNERBAR.**

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metadados de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





