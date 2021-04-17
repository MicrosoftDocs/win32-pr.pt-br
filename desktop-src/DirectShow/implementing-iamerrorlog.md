---
description: Implementando IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementando IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65eb968eb370d06fab6aca13af3215bb3b650257
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789640"
---
# <a name="implementing-iamerrorlog"></a>Implementando IAMErrorLog

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

A interface [**IAMErrorLog**](iamerrorlog.md) contém um único método, [**LogError**](iamerrorlog-logerror.md). Os parâmetros para o método contêm informações sobre o erro ocorrido.


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



O código de erro e a cadeia de caracteres de erro são definidos pelos serviços de edição do DirectShow. Para obter uma lista de erros, consulte [erros de renderização](rendering-errors.md).

O parâmetro *pExtraInfo* contém um ponteiro para um tipo Variant que contém informações adicionais sobre o erro. O tipo de dados e o conteúdo da variante dependem do erro específico que ocorreu. Por exemplo, se o erro foi causado por um nome de arquivo incorreto, a variante é uma cadeia de caracteres com o nome de arquivo inválido. Alguns erros não têm informações adicionais; portanto, *pExtraInfo* pode ser **nulo**. O código a seguir mostra como testar o membro **VT** da variante, que indica o tipo de dados e formatar uma mensagem de acordo.


```C++
if( pExtraInfo )    // Report extra information, if any. 
{                           
    printf("\tExtra info: ");
    if( pExtraInfo->vt == VT_BSTR )      // Extra info is a BSTR.
    {
        UINT len = SysStringLen(pExtraInfo->bstrVal);
        char *szExtra = new char[len];
        if (szExtra != NULL)
        {
            // Note - If the BSTR contains embedded NULL characters, this
            // will only pick up the first sub-string.
            WideCharToMultiByte(CP_ACP, 0, pExtraInfo->bstrVal, -1, 
                szExtra, len, 0, 0);
            printf("%s\n", szExtra);
            delete [] szExtra;
        }
    } 
    else if( pExtraInfo->vt == VT_I4 )   // Extra info is an integer.
        printf("%d\n", pExtraInfo->lVal);

    else if( pExtraInfo->vt == VT_R8 )   // Extra info is floating-point.
        printf("%f\n", pExtraInfo->dblVal);
}
```



> [!Note]  
> Não libere a variante apontada por
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>pExtraInfo</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> . Além disso, a variante torna-se inválida depois que o método retorna, portanto, não a referencie mais tarde.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros de log](logging-errors.md)
</dt> </dl>

 

 



