---
title: Considerações sobre Unicode
description: A função de serviço WriteFmtUserTypeStg, usada no método IPaper Save, requer parâmetros de cadeia de caracteres Unicode.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7bef75ec88318f4a2af8c5c7b693f0fc7c877f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822647"
---
# <a name="unicode-considerations"></a>Considerações sobre Unicode

A função de serviço **WriteFmtUserTypeStg** , usada no método [**IPaper:: Save**](ipaper--save.md) , requer parâmetros de cadeia de caracteres Unicode. Esse é o caso de chamadas de serviço COM/OLE que usam parâmetros de cadeia de caracteres. Ao compilar para cadeias de caracteres ANSI, os parâmetros Unicode esperados precisam de conversão de ANSI para Unicode. Esse processo é obtido usando algumas macros no APPUTIL. h que podem obscurecer conversões. Por exemplo, consulte **WriteFmtUserTypeStg**.

A chamada a seguir aparece no método [**Save**](ipaper--save.md) .


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Quando **StoServe** é compilado para ANSI (não para Unicode), essa chamada realmente reduz para uma chamada para uma função substituta interna APPUTIL. Para dar suporte a isso, o esquema de macro a seguir é usado em Apputil. h, que é um arquivo incluído em todos os exemplos de código. Arquivos CPP.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



O esquema usa funções de chamada de serviço substitutas. As versões ANSI das chamadas começam com um \_ . Essas funções ANSI substitutas são implementadas em Apputil. cpp. Eles são usados quando o exemplo de código está sendo compilado para cadeias de caracteres ANSI (o padrão nos makefiles). O serviço funciona de forma que os substitutos tenham suporte apenas a parâmetros de cadeia de caracteres Unicode. Isso força algumas conversões de cadeia de caracteres de ANSI para Unicode antes da chamada de serviço real COM/OLE ser feita dentro do substituto.

Por exemplo, se UNICODE não for definido durante a compilação, todas as chamadas nos exemplos para a função de serviço com **WriteFmtUserTypeStg** são realmente alteradas pelas macros em chamadas para uma \_ função WriteFmtUserTypeStg que é implementada em APPUTIL. CPP. Essa função aceita o ponteiro de cadeia de caracteres ANSI de entrada, converte-o em uma cópia Unicode e passa essa cópia Unicode como o parâmetro de cadeia de caracteres em uma chamada para a função **WriteFmtUserTypeStg** real.

Aqui está um \_ WriteFmtUserTypeStg de Apputil. cpp.

``` syntax
STDAPI A_WriteFmtUserTypeStg(
           IStorage* pIStorage,
           CLIPFORMAT ClipFmt,
           LPSTR pszUserType)
  {
    HRESULT hr = E_INVALIDARG;
    WCHAR wszUc[MAX_PATH];

    if (NULL != pszUserType)
    {
      // Convert from ANSI in pszUserType to Unicode in wszUc.
      AnsiToUc(pszUserType, wszUc, MAX_PATH);

      // Use the Unicode string in the actual service call.
      hr = WriteFmtUserTypeStg(pIStorage, ClipFmt, wszUc);
    }

    return hr;
  }
```

 

 




