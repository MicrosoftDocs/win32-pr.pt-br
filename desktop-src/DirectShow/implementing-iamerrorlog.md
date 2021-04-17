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
# <a name="implementing-iamerrorlog"></a><span data-ttu-id="8d2df-103">Implementando IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="8d2df-103">Implementing IAMErrorLog</span></span>

<span data-ttu-id="8d2df-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="8d2df-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8d2df-105">A interface [**IAMErrorLog**](iamerrorlog.md) contém um único método, [**LogError**](iamerrorlog-logerror.md).</span><span class="sxs-lookup"><span data-stu-id="8d2df-105">The [**IAMErrorLog**](iamerrorlog.md) interface contains a single method, [**LogError**](iamerrorlog-logerror.md).</span></span> <span data-ttu-id="8d2df-106">Os parâmetros para o método contêm informações sobre o erro ocorrido.</span><span class="sxs-lookup"><span data-stu-id="8d2df-106">The parameters to the method contain information about the error that occurred.</span></span>


```C++
STDMETHODIMP LogError(
    LONG Severity,          // Reserved. Do not use.
    BSTR ErrorString,       // Description.
    LONG ErrorCode,         // Error code.
    HRESULT hresult,        // HRESULT that caused the error.
    VARIANT *pExtraInfo);   // Extra information about the error.
```



<span data-ttu-id="8d2df-107">O código de erro e a cadeia de caracteres de erro são definidos pelos serviços de edição do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8d2df-107">The error code and the error string are defined by DirectShow Editing Services.</span></span> <span data-ttu-id="8d2df-108">Para obter uma lista de erros, consulte [erros de renderização](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="8d2df-108">For a list of errors, see [Rendering Errors](rendering-errors.md).</span></span>

<span data-ttu-id="8d2df-109">O parâmetro *pExtraInfo* contém um ponteiro para um tipo Variant que contém informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="8d2df-109">The *pExtraInfo* parameter contains a pointer to a VARIANT type that holds additional information about the error.</span></span> <span data-ttu-id="8d2df-110">O tipo de dados e o conteúdo da variante dependem do erro específico que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="8d2df-110">The data type and contents of the VARIANT depend on the specific error that occurred.</span></span> <span data-ttu-id="8d2df-111">Por exemplo, se o erro foi causado por um nome de arquivo incorreto, a variante é uma cadeia de caracteres com o nome de arquivo inválido.</span><span class="sxs-lookup"><span data-stu-id="8d2df-111">For example, if the error was caused by an incorrect file name, the VARIANT is a string with the bad file name.</span></span> <span data-ttu-id="8d2df-112">Alguns erros não têm informações adicionais; portanto, *pExtraInfo* pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8d2df-112">Some errors do not have extra information, so *pExtraInfo* might be **NULL**.</span></span> <span data-ttu-id="8d2df-113">O código a seguir mostra como testar o membro **VT** da variante, que indica o tipo de dados e formatar uma mensagem de acordo.</span><span class="sxs-lookup"><span data-stu-id="8d2df-113">The following code shows how to test the **vt** member of the VARIANT, which indicates the data type, and format a message accordingly.</span></span>


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
> <span data-ttu-id="8d2df-114">Não libere a variante apontada por</span><span class="sxs-lookup"><span data-stu-id="8d2df-114">Do not free the VARIANT pointed to by</span></span>
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
> <span data-ttu-id="8d2df-115">.</span><span class="sxs-lookup"><span data-stu-id="8d2df-115">.</span></span> <span data-ttu-id="8d2df-116">Além disso, a variante torna-se inválida depois que o método retorna, portanto, não a referencie mais tarde.</span><span class="sxs-lookup"><span data-stu-id="8d2df-116">Also, the VARIANT becomes invalid after the method returns, so do not reference it later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8d2df-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d2df-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d2df-118">Erros de log</span><span class="sxs-lookup"><span data-stu-id="8d2df-118">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



