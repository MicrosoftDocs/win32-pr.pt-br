---
title: atributo optimize
description: O atributo \ optimize\ ACF é usado para ajustar o nível de gradação para marshaling de dados.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- otimizar atributo MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7703a3539ff16c7f2dc78d51c62cfe05612dcb6e935bb5c5701f9a7b59a9f1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869566"
---
# <a name="optimize-attribute"></a>atributo optimize

O **\[ atributo \]** optimize ACF é usado para ajustar o nível de gradação para marshaling de dados.

> [!Note]  
> Essa palavra-chave é superada e não deve ser usada. As compilações MIDL atuais devem usar [**/Oicf**](-oi.md)[**/robust.**](-robust.md)

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*opções de otimização* 
</dt> <dd>

Especifica o método de marshaling de dados. Use "s" para marshaling de modo misto ou "i" para marshaling interpretado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta versão do RPC fornece dois métodos para marshaling de dados: modo misto ("s") e interpretado ("i"). Esses métodos correspondem às opções de linha de [**comando /Os**](-os.md) e [**/Oi.**](-oi.md) O método interpretado marshals de dados completamente offline. Embora isso possa reduzir consideravelmente o tamanho do stub, o desempenho pode ser afetado.

Se o desempenho for uma preocupação, o método de modo misto poderá ser a melhor abordagem. O modo misto permite que o compilador MIDL faça a determinação entre quais dados serão empacotados em linha e quais serão empacotados por uma chamada para uma biblioteca de vínculo dinâmico offline. Se muitos procedimentos usarem os mesmos tipos de dados, um único procedimento poderá ser chamado repetidamente para fazer marshal dos dados. Dessa forma, os dados mais adequados para marshaling em linha são processados em linha, enquanto outros dados podem ter marshaling offline mais eficiente.

Observe que o **\[ atributo optimize \]** pode ser usado como um atributo de interface ou como um atributo de operação. Se for usado como um atributo de interface, ele define o padrão para toda a interface, substituindo opções de linha de comando. Se, no entanto, ele for usado como um atributo de operação, afetará apenas essa operação, substituindo as opções de linha de comando e o padrão da interface.

## <a name="examples"></a>Exemplos

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**/os**](-os.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




