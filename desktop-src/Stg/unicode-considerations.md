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
# <a name="unicode-considerations"></a><span data-ttu-id="e4942-103">Considerações sobre Unicode</span><span class="sxs-lookup"><span data-stu-id="e4942-103">Unicode Considerations</span></span>

<span data-ttu-id="e4942-104">A função de serviço **WriteFmtUserTypeStg** , usada no método [**IPaper:: Save**](ipaper--save.md) , requer parâmetros de cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="e4942-104">The **WriteFmtUserTypeStg** service function, used in the [**IPaper::Save**](ipaper--save.md) method, requires Unicode string parameters.</span></span> <span data-ttu-id="e4942-105">Esse é o caso de chamadas de serviço COM/OLE que usam parâmetros de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e4942-105">This is the case with COM/OLE service calls that take string parameters.</span></span> <span data-ttu-id="e4942-106">Ao compilar para cadeias de caracteres ANSI, os parâmetros Unicode esperados precisam de conversão de ANSI para Unicode.</span><span class="sxs-lookup"><span data-stu-id="e4942-106">When compiling for ANSI strings, the expected Unicode parameters need conversion from ANSI to Unicode.</span></span> <span data-ttu-id="e4942-107">Esse processo é obtido usando algumas macros no APPUTIL. h que podem obscurecer conversões.</span><span class="sxs-lookup"><span data-stu-id="e4942-107">This process is achieved using some macros in APPUTIL.h that may obscure conversions.</span></span> <span data-ttu-id="e4942-108">Por exemplo, consulte **WriteFmtUserTypeStg**.</span><span class="sxs-lookup"><span data-stu-id="e4942-108">For example, see **WriteFmtUserTypeStg**.</span></span>

<span data-ttu-id="e4942-109">A chamada a seguir aparece no método [**Save**](ipaper--save.md) .</span><span class="sxs-lookup"><span data-stu-id="e4942-109">The following call appears in the [**Save**](ipaper--save.md) method.</span></span>


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



<span data-ttu-id="e4942-110">Quando **StoServe** é compilado para ANSI (não para Unicode), essa chamada realmente reduz para uma chamada para uma função substituta interna APPUTIL.</span><span class="sxs-lookup"><span data-stu-id="e4942-110">When **StoServe** is compiled for ANSI (not for Unicode), this call actually reduces to a call to an internal APPUTIL surrogate function.</span></span> <span data-ttu-id="e4942-111">Para dar suporte a isso, o esquema de macro a seguir é usado em Apputil. h, que é um arquivo incluído em todos os exemplos de código. Arquivos CPP.</span><span class="sxs-lookup"><span data-stu-id="e4942-111">To support this, the following macro scheme is used in Apputil.h, which is an included file in all code sample .CPP files.</span></span>


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



<span data-ttu-id="e4942-112">O esquema usa funções de chamada de serviço substitutas.</span><span class="sxs-lookup"><span data-stu-id="e4942-112">The scheme uses surrogate service call functions.</span></span> <span data-ttu-id="e4942-113">As versões ANSI das chamadas começam com um \_ .</span><span class="sxs-lookup"><span data-stu-id="e4942-113">The ANSI versions of the calls begin with A\_.</span></span> <span data-ttu-id="e4942-114">Essas funções ANSI substitutas são implementadas em Apputil. cpp.</span><span class="sxs-lookup"><span data-stu-id="e4942-114">These surrogate ANSI functions are implemented in Apputil.cpp.</span></span> <span data-ttu-id="e4942-115">Eles são usados quando o exemplo de código está sendo compilado para cadeias de caracteres ANSI (o padrão nos makefiles).</span><span class="sxs-lookup"><span data-stu-id="e4942-115">They are used when the code sample is being compiled for ANSI strings (the default in the makefiles).</span></span> <span data-ttu-id="e4942-116">O serviço funciona de forma que os substitutos tenham suporte apenas a parâmetros de cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="e4942-116">The service functions that the surrogates stand in place of support only Unicode string parameters.</span></span> <span data-ttu-id="e4942-117">Isso força algumas conversões de cadeia de caracteres de ANSI para Unicode antes da chamada de serviço real COM/OLE ser feita dentro do substituto.</span><span class="sxs-lookup"><span data-stu-id="e4942-117">This forces some string conversions from ANSI to Unicode before the real COM/OLE service call is made inside the surrogate.</span></span>

<span data-ttu-id="e4942-118">Por exemplo, se UNICODE não for definido durante a compilação, todas as chamadas nos exemplos para a função de serviço com **WriteFmtUserTypeStg** são realmente alteradas pelas macros em chamadas para uma \_ função WriteFmtUserTypeStg que é implementada em APPUTIL. CPP.</span><span class="sxs-lookup"><span data-stu-id="e4942-118">For example, if UNICODE is not defined during compiling, any calls in the samples to the **WriteFmtUserTypeStg** COM service function are actually changed by the macros into calls to an A\_WriteFmtUserTypeStg function that is implemented in APPUTIL.CPP.</span></span> <span data-ttu-id="e4942-119">Essa função aceita o ponteiro de cadeia de caracteres ANSI de entrada, converte-o em uma cópia Unicode e passa essa cópia Unicode como o parâmetro de cadeia de caracteres em uma chamada para a função **WriteFmtUserTypeStg** real.</span><span class="sxs-lookup"><span data-stu-id="e4942-119">This function accepts the input ANSI string pointer, converts it to a Unicode copy, and passes that Unicode copy as the string parameter in a call to the actual **WriteFmtUserTypeStg** function.</span></span>

<span data-ttu-id="e4942-120">Aqui está um \_ WriteFmtUserTypeStg de Apputil. cpp.</span><span class="sxs-lookup"><span data-stu-id="e4942-120">Here is A\_WriteFmtUserTypeStg from Apputil.cpp.</span></span>

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

 

 




