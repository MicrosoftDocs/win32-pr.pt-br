---
title: comutador/sal
description: A opção/sal direciona MIDL para gerar anotações SAL nos arquivos stub gerados.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- MIDL do comutador/sal
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105748788"
---
# <a name="sal-switch"></a>comutador/sal

A opção **/sal** direciona MIDL para gerar anotações sal nos arquivos stub gerados.

``` syntax
midl /sal
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

MIDL marcará os parâmetros de ponteiro e de matriz com anotações que refletem a descrição do parâmetro no arquivo IDL conforme imposto pelo RPC e pelo mecanismo de marshaling do NDR. MIDL não cria anotações para parâmetros em métodos de interface marcados com o atributo [**\[ local \]**](local.md), a menos que [**/sal \_ local**](-sal-local.md) também esteja presente na linha de comando. Para substituir a anotação gerada por MIDL, use o atributo [**\[ anotar \]**](annotate.md) .

As anotações geradas por MIDL são sempre prefixadas com \_ \_ RPC \_ e exigem o uso do cabeçalho **RPCs. h** para traduzir a anotação em anotações sal padrão.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal \_ local**](-sal-local.md)
</dt> <dt>

[**\[anotar\]**](annotate.md)
</dt> </dl>

 

 




