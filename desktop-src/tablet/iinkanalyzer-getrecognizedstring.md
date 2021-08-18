---
description: Recupera a cadeia de caracteres de melhor resultado da operação de reconhecimento para toda a árvore de nós de contexto no IInkAnalyzer.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: Método IInkAnalyzer::GetRecognizedString (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3defa68f68e0c2e81bdb093005db1e173442b9686ca4c98a4966c755b2fb52dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092244"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a>Método IInkAnalyzer::GetRecognizedString

Recupera a cadeia de caracteres de melhor resultado da operação de reconhecimento para toda a árvore de nós de contexto no [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbstrRecognizedString* \[ out\]
</dt> <dd>

A cadeia de caracteres de melhor resultado da operação de reconhecimento para toda a árvore de nós de contexto no [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para *pbstrRecognizedString* quando você não precisar mais usar a cadeia de caracteres.

 

Esse método retorna o mesmo valor que os dados de propriedade do nó raiz para a cadeia de caracteres reconhecida. (Consulte [**Método IInkAnalyzer::GetRootNode,**](iinkanalyzer-getrootnode.md) [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)e [Propriedades do Nó de Contexto](context-node-properties.md).)

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra um método que orienta a árvore de resultados [**IContextNode**](icontextnode.md) do analisador de tinta. Se o IInkAnlyzer não estiver executando a análise de tinta no momento, o método faz o seguinte.

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

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

