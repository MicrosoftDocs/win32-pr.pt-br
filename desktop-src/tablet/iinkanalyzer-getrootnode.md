---
description: Obtém o IContextNode raiz da árvore de contexto do objeto IInkAnalyzer.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: Método IInkAnalyzer::GetRootNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5ff2181eacd3df1d2815448a0c2d7cafce4d521fa0abbc7b26492d9c078982dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713415"
---
# <a name="iinkanalyzergetrootnode-method"></a>Método IInkAnalyzer::GetRootNode

Obtém o [**IContextNode raiz**](icontextnode.md) da árvore de contexto do objeto [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppRootNode* \[ out\]
</dt> <dd>

O [**IContextNode raiz**](icontextnode.md) da árvore de contexto do objeto [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppRootNode* quando você não precisar mais usar o nó raiz.

 

O [**IInkAnalyzer**](iinkanalyzer.md) mantém uma árvore de [**objetos IContextNode.**](icontextnode.md) Esses objetos contêm a entrada para análise e os resultados da análise. Quando os traços são inicialmente adicionados ao **IInkAnalyzer**, o **IInkAnalyzer** os atribui a **um IContextNode** do tipo UnclassifiedInk (consulte [**IContextNode::GetType**](icontextnode-gettype.md) e Tipos de Nó de Contexto [).](context-node-types.md) Depois que os traços são analisados, **o IInkAnalyzer** os atribui a objetos **IContextNode** apropriados na árvore. Para obter mais informações sobre como usar **o IInkAnalyzer para** analisar tinta, consulte Visão [geral da análise de tinta.](ink-analysis-overview.md)

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

