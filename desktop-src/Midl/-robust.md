---
title: comutador/robust
description: A opção/robust informa o compilador MIDL para gerar informações adicionais de verificação de erros, que o mecanismo de NDR usa para executar verificações de integridade em tempo de execução.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- MIDL do comutador/robust
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551f5a60013aa3a903dcb3e35cc4c25a9f83dc67fff2a6ab5c7bfd62a041feee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895816"
---
# <a name="robust-switch"></a>comutador/robust

A opção **/robust** informa o compilador MIDL para gerar informações adicionais de verificação de erros, que o mecanismo de NDR usa para executar verificações de integridade em tempo de execução.

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/OIF* 
</dt> <dd>

Essas opções são idênticas em sua funcionalidade. Eles especificam o método de proxy com código de marshaling e usam cadeias de caracteres de formato rápido para melhorar o desempenho. Consulte/ [**Oi**](-oi.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

O uso da opção **/robust** gera informações adicionais que permitem que o mecanismo de representação de dados de rede (NDR) execute a verificação de erros em tempo de execução em argumentos correlacionados em matrizes dinâmicas, uniões e ponteiros [**de interface em**](out-idl.md) aplicativos DCOM. A opção **/robust** só está disponível no WindowsÂ 2000 e versões posteriores do Windows.

Um argumento correlacionado é um argumento que usa qualquer um dos atributos que permitem que o tamanho de um objeto de dados seja determinado em tempo de execução: o [**tamanho \_ é**](size-is.md), o [**comprimento \_ é**](length-is.md), o [**primeiro \_ é**](first-is.md), o [**último \_ é**](last-is.md), o [**máximo \_ é**](max-is.md), o [**switch \_ é**](switch-is.md)e o [**IID \_ é**](iid-is.md). De acordo com a especificação uso-DCE para a representação de transmissão, esse argumento correlacionado aparece em dois locais diferentes. Por exemplo, considere um uso típico do **tamanho como \_** atributo:

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

Neste exemplo, o cliente passa um Long que especifica o tamanho de um bloco de tipos de barra \_ (em termos de número de elementos de tipos de barra \_ ) e um ponteiro para o bloco real de \_ tipos de barra. O argumento size se correlaciona com o argumento pBarType. De acordo com a especificação uso-DCE, o argumento Size é representado duas vezes na transmissão, primeiro como em si e, em seguida, com a matriz de elementos de tipo de barra \_ que representam o argumento pBarType. Cada argumento é desempacotado de forma independente, de acordo com sua própria representação de conexão. Normalmente, o argumento size e sua cópia, que é usada para representar parte do outro argumento, têm os mesmos valores. No entanto, se o argumento de tamanho se tornar corrompido (por exemplo, quando o bloco de tipos de barra \_ for maior do que o que foi alocado), o aplicativo de servidor poderá parar de responder, pois ele usa o valor do argumento size para medir os dados de entrada.

A opção **/robust** é necessária para implementar a verificação de intervalo válida com o atributo [**Range**](range.md) .

## <a name="examples"></a>Exemplos

**MIDL/robust/Oicf filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**amplitude**](range.md)
</dt> </dl>

 

 




