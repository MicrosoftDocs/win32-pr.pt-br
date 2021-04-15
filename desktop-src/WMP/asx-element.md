---
title: Elemento ASX
description: O elemento ASX define um arquivo como um metarquivo.
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
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760898"
---
# <a name="asx-element"></a>Elemento ASX

O elemento **ASX** define um arquivo como um metarquivo.

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

Número decimal que representa o número de versão da sintaxe para o metarquivo. Defina como 3 ou 3,0.

**Modo de exibição de visualização** (opcional)

Valor que indica se o Windows Media Player entra no modo de visualização antes de reproduzir o primeiro clipe.

Deve ser um dos valores a seguir.



| Valor | Descrição                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | O Windows Media Player entra no modo de visualização antes de executar o primeiro clipe.                            |
| Não    | O valor padrão. O Windows Media Player não entra no modo de visualização antes de executar o primeiro clipe. |



 

**BANNERBAR** (opcional)

Valor que indica se o Windows Media Player reserva espaço para um gráfico de faixa.

Deve ser um dos valores a seguir.



| Valor | Descrição                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | O valor padrão. O Windows Media Player reserva espaço para a barra de faixa somente quando uma parte do conteúdo inclui uma.                       |
| FIXED | O Windows Media Player reserva um espaço fixo para um gráfico de banner para cada parte do conteúdo tocado, independentemente de haver uma faixa associada. |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai | Nenhum. O elemento **ASX** deve ser o primeiro elemento em todos os metarquivos.                                                                                                 |
| Elementos filho  | **abstrato**, **autor**, **faixa**, **base**, **direitos autorais**, **entrada**, **ENTRYREF**, **evento**, **moreinfo**, **PREVIEWDURATION**, **param**, **repetir**, **título** |



 

## <a name="remarks"></a>Comentários

Os primeiros quatro caracteres de uma lista de reprodução de metarquivo devem ser "<ASX". Outros elementos definidos no escopo do elemento **ASX** , como **título** e **autor**, são associados à exibição de informações exibidas pelo Windows Media Player.

Para o Windows Media Player, o número de versão da sintaxe é 3,0. O Windows Media Player dá suporte a todas as versões anteriores da sintaxe de metarquivo. Os valores aceitáveis para o atributo **version** incluem 3,0 e 3 (sem ponto decimal).

Se o valor do atributo **PREviewmode** for sim, o Windows Media Player entrará imediatamente no modo de visualização antes de reproduzir o primeiro clipe. Quando o Windows Media Player entra no modo de visualização, ele visualiza cada clipe referenciado no metarquivo. O elemento **PREVIEWDURATION** determina a duração de cada visualização.

O atributo **BANNERBAR** define se o player de mídia do Windows reserva espaço para um gráfico de faixa. Uma faixa é um gráfico que é exibido na área de exibição do vídeo enquanto o conteúdo da mídia está sendo reproduzido. (Use o elemento **banner** para adicionar uma faixa ao conteúdo.) Se o valor de **BANNERBAR** for corrigido, o Windows Media Player reserva espaço em faixa para cada parte do conteúdo de mídia, independentemente de o conteúdo de mídia ter uma faixa. Se uma parte do conteúdo de mídia não tiver uma faixa associada a ela, o espaço reservado para um será preto. Se o valor do atributo **BANNERBAR** for auto, o Windows Media Player reserva espaço para a faixa somente quando o conteúdo da mídia inclui um.

Se você criar um metarquivo com vários clipes (elementos de **entrada** ou **ENTRYREF** ) e definir o valor do atributo **BANNERBAR** como auto, o Windows Media Player poderá ser redimensionado para permitir espaço para um gráfico de faixa para um clipe e redimensioná-lo novamente se o próximo clipe não contiver um gráfico de faixa. Se você quiser que o tamanho da janela permaneça o mesmo (exceto quando o tamanho do vídeo for alterado), use o valor fixo para o atributo **BANNERBAR** .

O espaço reservado para um gráfico de banner é de 32 pixels de altura por 194 pixels de largura. O espaço reservado é exibido abaixo de qualquer conteúdo de vídeo renderizado e 6 pixels acima da borda inferior da área de vídeo, permitindo o espaço para a borda da área de vídeo de 6 pixels. O espaço reservado da faixa é centralizado horizontalmente.

O Windows Media Player renderiza o gráfico a partir do pixel da extrema esquerda do espaço do banner. Se o gráfico ocupar todo o espaço, ele aparecerá centralizado horizontalmente. Caso contrário, haverá espaço à direita. Observe que a largura mínima do Windows Media Player é sempre maior do que o tamanho do clipe de vídeo, independentemente do valor do atributo **BANNERBAR** .

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

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





