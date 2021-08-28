---
description: Implementando IAMErrorLog
ms.assetid: 0a380854-f3a9-4077-a481-dda67737d4c8
title: Implementando IAMErrorLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de0ab694b2e2b8868717b6b4c11b2124ecc4042
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982199"
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



o código de erro e a cadeia de caracteres de erro são definidos por DirectShow serviços de edição. Para obter uma lista de erros, consulte [erros de renderização](rendering-errors.md).

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
> 
>
> 
| Rótulo | Valor |
|--------|-------|
| <pre><code>pExtraInfo</code></pre> | 

>
> 
>
> . Além disso, a variante torna-se inválida depois que o método retorna, portanto, não a referencie mais tarde.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros de log](logging-errors.md)
</dt> </dl>

 

 



