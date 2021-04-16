---
title: otimizar atributo
description: O atributo \ Optimize \ ACF é usado para ajustar o nível de gradação para o marshaling de dados.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- otimizar o atributo MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105750020"
---
# <a name="optimize-attribute"></a>otimizar atributo

O atributo **\[ Optimize \]** ACF é usado para ajustar o nível de gradação de dados de marshaling.

> [!Note]  
> Essa palavra-chave é superceeded e não deve ser usada. Compilações de MIDL atuais devem usar [**/Oicf**](-oi.md)[**/robust**](-robust.md) em vez disso.

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*otimização – opções* 
</dt> <dd>

Especifica o método de marshaling de dados. Use "s" para o marshaling de modo misto ou "i" para o marshaling interpretado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta versão do RPC fornece dois métodos para empacotamento de dados: modo misto ("s") e interpretado ("i"). Esses métodos correspondem às opções de linha de comando [**/os**](-os.md) e [**/Oi**](-oi.md) . O método interpretado realiza marshaling de dados completamente offline. Embora isso possa reduzir consideravelmente o tamanho do stub, o desempenho pode ser afetado.

Se o desempenho for uma preocupação, o método de modo misto poderá ser a melhor abordagem. O modo misto permite que o compilador MIDL faça a determinação entre quais dados serão empacotados embutidos e que serão empacotados por uma chamada para uma biblioteca de vínculo dinâmico offline. Se muitos procedimentos usarem os mesmos tipos de dados, um único procedimento poderá ser chamado repetidamente para empacotar os dados. Dessa forma, os dados mais adequados para o marshaling embutido são processados em linha, enquanto outros dados podem ser empacotados com mais eficiência offline.

Observe que o atributo **\[ Optimize \]** pode ser usado como um atributo de interface ou como um atributo de operação. Se ele for usado como um atributo de interface, ele definirá o padrão para a interface inteira, substituindo opções de linha de comando. No entanto, se ele for usado como um atributo de operação, ele afetará apenas essa operação, substituindo as opções de linha de comando e o padrão da interface.

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

[**/Os**](-os.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




