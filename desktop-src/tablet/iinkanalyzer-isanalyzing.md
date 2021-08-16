---
description: Recupera um valor que indica se o IInkAnalyzer está executando a análise de tinta.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: Método IInkAnalyzer::IsAnalyzing (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1dc0a10bfcafb5972413eb1d1d0880a63db69498c38481cc0cbf6bb58e5f69f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092046"
---
# <a name="iinkanalyzerisanalyzing-method"></a>Método IInkAnalyzer::IsAnalyzing

Recupera um valor que indica se [**o IInkAnalyzer**](iinkanalyzer.md) está executando a análise de tinta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbAnalyzing* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** se o [**IInkAnalyzer**](iinkanalyzer.md) estiver executando a análise de tinta; caso contrário, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Essa propriedade será **VARIANT \_ TRUE** se [**o IInkAnalyzer**](iinkanalyzer.md) estiver executando uma análise síncrona ou assíncrona.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra um método que orienta a árvore de resultados [**IContextNode**](icontextnode.md) do analisador de tinta. Se o analisador de tinta não estiver executando a análise de tinta no momento, o método faz o seguinte.

-   Obtém a cadeia de caracteres de reconhecimento superior.
-   Obtém o nó raiz do analisador de tinta.
-   Chama um método auxiliar, `ExploreContextNode` , para examinar o nó raiz e seus nós filho.


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
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

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




