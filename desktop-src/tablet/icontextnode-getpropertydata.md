---
description: Recupera dados específicos do aplicativo ou outros dados de propriedade para o identificador especificado.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'Método IContextNode:: GetPropertyData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647236"
---
# <a name="icontextnodegetpropertydata-method"></a>Método IContextNode:: GetPropertyData

Recupera dados específicos do aplicativo ou outros dados de propriedade para o identificador especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPropertyDataId* \[ no\]
</dt> <dd>

O identificador dos dados.

</dd> <dt>

*pulPropertyDataSize* \[ entrada, saída\]
</dt> <dd>

O tamanho dos dados em bytes. O valor que é passado não é usado.

</dd> <dt>

*ppbPropertyData* \[ fora\]
</dt> <dd>

Um ponteiro para uma matriz de inteiros sem sinal de 8 bits que contém os dados de propriedade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppbPropertyData* quando você não precisar mais das informações.

 

Além de recuperar dados específicos do aplicativo que foram adicionados com [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md), esse método é usado para recuperar propriedades comuns que são descritas pelas constantes de [Propriedades do nó de contexto](context-node-properties.md) .

As propriedades do tipo de cadeia de caracteres incluem:

-   GUID \_ CNP \_ reconhecívelstring
-   GUID \_ CNP \_ FormatName
-   GUID \_ AHP \_ ANALYSISHINTNAME
-   GUID \_ AHP \_ PREFIXTEXT
-   GUID \_ AHP \_ SUFFIXTEXT
-   \_factor de AHP GUID \_

O valor de retorno é ** \* WCHAR*_. Se você converter o \_ parâmetro *ppbPropertyData* para **WCHAR \**_ , seu comprimento retornado será `(length of the string + 1) _ sizeof(WCHAR)` .

As propriedades do tipo booliano incluem:

-   GUID \_ AHP \_ OVERRIDELANGUAGEID
-   GUID \_ AHP \_ COERCETOFACTOID
-   GUID \_ AHP \_ WordMode

O valor de retorno **é \_ booliano de Variant**. Se você converter o \* parâmetro *ppbPropertyData* para **Variant \_ bool \** _, seu comprimento retornado será `sizeof(VARIANT_BOOL)` .

GUID \_ AHP \_ guia é uma propriedade do tipo guia. O valor de retorno _*é \* InkAnalysisRecognitionGuide*_. Se você converter o \_ parâmetro *ppbPropertyData* para **InkAnalysisRecognitionGuide \**, seu comprimento retornado será `sizeof(InkAnalysisRecognitionGuide)` .

As propriedades do tipo inteiro incluem:

-   GUID \_ CNP \_ LINENUMBER
-   GUID \_ CNP \_ POINTSPERINCH
-   GUID \_ CNP \_ CONFIDENCELEVEL
-   \_confirmação de CNP GUID \_
-   GUID \_ CNP \_ MAXIMUMSTROKECOUNT
-   \_segmentação de CNP GUID \_
-   GUID \_ CNP \_ ALIGNMENTLEVEL

O valor de retorno _*é \* longo*_. Se você converter o \_ parâmetro *ppbPropertyData* para **Long \** _, seu comprimento retornado será `sizeof(LONG)` .

Métricas de linha – as propriedades do tipo incluem:

-   GUID \_ CNP \_ ascendentes
-   GUID \_ CNP \_ descendentes
-   \_linha de \_ base CNP GUID
-   GUID \_ CNP \_ Tabs no meio

O valor de retorno _*é \* longo*_. Se você converter o \_ parâmetro *ppbPropertyData* para **Long \** _, seu comprimento retornado será `sizeof(LONG)_4` , significando os valores (x, y) para os pontos iniciais seguidos dos valores (x, y) dos pontos finais.

GUID \_ CNP \_ TEXTRECOGNIZERID é uma propriedade **GUID** . O valor de retorno é ** \* GUID*_. Se você converter o \_ parâmetro *ppbPropertyData* para **GUID \** ,_ seu comprimento retornado será `sizeof(GUID)` .

GUID \_ CNP \_ ROTATEDBOUNDINGBOX é uma propriedade de caixa delimitadora girada. O valor de retorno _*é \* longo*_. Se você converter o \_ parâmetro *ppbPropertyData* para **Long \** _, seu comprimento retornado será `sizeof(LONG)_8` , significando os valores (x, y) para os quatro cantos da caixa.

GUID \_ CNP \_ HOTPOINT é uma propriedade de ponto de acesso. O valor de retorno é ** \* Long*_. Se você converter o \_ parâmetro *ppbPropertyData* para **longo \**_ seu comprimento retornado é `sizeof(LONG)_2` , significando os valores (x, y) para o ponto.

\_O AHP \_ de palavras do GUID é uma propriedade da lista de palavras. O valor de retorno é ** \* WCHAR*_. Se você converter o \_ parâmetro *ppbPropertyData* para **WCHAR \**_ , seu comprimento retornado será `n _ sizeof(WCHAR)` , em que `n` é a soma dos comprimentos das cadeias de caracteres do número de cadeias na lista mais 1 para cada caractere de término **nulo** para cada cadeia de caracteres.

## <a name="examples"></a>Exemplos

Este exemplo mostra um método que acessa a propriedade do nó de contexto AlignmentLevel de um tipo de nó de contexto de parágrafo.


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

