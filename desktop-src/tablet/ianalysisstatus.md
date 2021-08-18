---
description: Representa o status da operação de análise de tinta, descrevendo se a análise foi concluída com êxito e se algum aviso ocorreu.
ms.assetid: 57910a1d-3472-4689-ba0d-a220145e77c4
title: Interface IAnalysisStatus (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 006b042981392ecdd52508181c7a5cde270d2e0195fe9c8b971c142361ab6081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719993"
---
# <a name="ianalysisstatus-interface"></a>Interface IAnalysisStatus

Representa o status da operação de análise de tinta, descrevendo se a análise foi concluída com êxito e se algum aviso ocorreu.

## <a name="members"></a>Membros

A interface **IAnalysisStatus** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisStatus** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IAnalysisStatus** tem esses métodos.



| Método                                                                     | Descrição                                                                                                                                                                                    |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAppliedChangesRegion**](ianalysisstatus-getappliedchangesregion.md) | Recupera a região do documento que corresponde às alterações feitas na árvore de nós de contexto do objeto [**IInkAnalyzer**](iinkanalyzer.md) como resultado da análise de tinta.<br/> |
| [**GetWarnings**](ianalysisstatus-getwarnings.md)                         | Recupera uma [**coleção IAnalysisWarnings**](ianalysiswarnings.md) que descreve todos os erros e avisos gerados pela operação de análise.<br/>                                  |
| [**IsSuccessful**](ianalysisstatus-issuccessful.md)                       | Recupera um resumo booliana dos resultados da operação de análise.<br/>                                                                                                               |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra um contorno de um manipulador de eventos para [**\_ o evento IAnalysisEvents::Results.**](-ianalysisevents-results.md) O manipulador verifica [**IAnalysisStatus::IsSuccessful.**](ianalysisstatus-issuccessful.md) Se a operação de análise gerar avisos, o manipulador itera pela coleção de [**objetos IAnalysisWarning.**](ianalysiswarning.md)


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
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

