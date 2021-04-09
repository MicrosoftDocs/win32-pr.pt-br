---
description: Representa um aviso ou erro que ocorre durante uma operação de análise de tinta.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interface IAnalysisWarning (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090554"
---
# <a name="ianalysiswarning-interface"></a>Interface IAnalysisWarning

Representa um aviso ou erro que ocorre durante uma operação de análise de tinta.

## <a name="members"></a>Membros

A interface **IAnalysisWarning** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisWarning** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAnalysisWarning** tem esses métodos.



| Método                                                            | Descrição                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBackgroundError**](ianalysiswarning-getbackgrounderror.md) | Recupera o código de erro para a operação de análise de tinta em segundo plano se ocorreu um erro.<br/>                                    |
| [**Gethint**](ianalysiswarning-gethint.md)                       | Recupera a dica de análise que causou este aviso<br/>                                                                        |
| [**GetNodeIds**](ianalysiswarning-getnodeids.md)                 | Recupera os identificadores de todos os nós de contexto relevantes associados a este aviso.<br/>                              |
| [**GetWarningCode**](ianalysiswarning-getwarningcode.md)         | Recupera o tipo de aviso que ocorreu usando a enumeração [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .<br/> |



 

## <a name="remarks"></a>Comentários

Os tipos de avisos que podem ocorrer são descritos pela enumeração [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) . Geralmente, os avisos ocorrem quando você tenta usar um recurso que não é suportado pelo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que o [**IInkAnalyzer**](iinkanalyzer.md) está usando.

Alguns avisos indicam que o [**IInkAnalyzer**](iinkanalyzer.md) não concluiu a operação de análise. Para obter mais informações, consulte [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra um contorno de um manipulador de eventos para o evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) . O manipulador verifica [**IAnalysisStatus:: Issuccessfully**](ianalysisstatus-issuccessful.md). Se a operação de análise gerar avisos, o manipulador iterará pela coleção de objetos **IAnalysisWarning** .


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisWarnings**](ianalysiswarnings.md)
</dt> <dt>

[**AnalysisWarningCode**](analysiswarningcode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

