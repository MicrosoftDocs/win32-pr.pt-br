---
description: Recupera os resultados da análise do objeto InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: Função CallDivideResults
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089706"
---
# <a name="calldivideresults-function"></a>Função CallDivideResults

Recupera os resultados da análise do objeto [**InkDivider**](inkdivider-class.md) .

Esta função não se destina a ser usada pelo código do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDivider* \[ no\]
</dt> <dd>

Um identificador para o objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aWordStrokeIds* \[ fora\]
</dt> <dd>

Uma matriz de identificadores associada à palavra que é passada para a classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aLineStrokeIds* \[ fora\]
</dt> <dd>

Uma matriz de propriedades de [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associados à linha que é passada para a classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aParagraphStrokeIds* \[ fora\]
</dt> <dd>

Uma matriz das propriedades de [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associados ao parágrafo da classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*aDrawingStrokeIds* \[ fora\]
</dt> <dd>

Uma matriz de propriedades de [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associados ao desenho da classe [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pastrWords* \[ fora\]
</dt> <dd>

Uma matriz de palavras retornada da análise de tinta.

</dd> <dt>

*pastrLines* \[ fora\]
</dt> <dd>

Uma matriz de linhas retornadas da análise de tinta.

</dd> <dt>

*pastrParagraphs* \[ fora\]
</dt> <dd>

Uma matriz de parágrafos retornada da análise de tinta.

</dd> <dt>

*aWordRotationCenterX* \[ fora\]
</dt> <dd>

Uma matriz dos pontos centrais das palavras ao longo do eixo x da análise de tinta.

</dd> <dt>

*aWordRotationCenterY* \[ fora\]
</dt> <dd>

Uma matriz dos pontos centrais das palavras ao longo do eixo y da análise de tinta.

</dd> <dt>

*aWordAngle* \[ fora\]
</dt> <dd>

Uma matriz que contém os ângulos pelos quais girar as palavras para obter melhores resultados de análise.

</dd> <dt>

*aLineRotationCenterX* \[ fora\]
</dt> <dd>

Uma matriz que contém os pontos centrais das linhas ao longo do eixo x.

</dd> <dt>

*aLineRotationCenterY* \[ fora\]
</dt> <dd>

Uma matriz que contém os pontos centrais das linhas ao longo do eixo y.

</dd> <dt>

*aLineAngle* \[ fora\]
</dt> <dd>

Uma matriz que contém os ângulos pelos quais girar as linhas para obter melhores resultados de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A função foi bem-sucedida.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *hDivider* é inválido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não foi possível alocar memória suficiente para armazenar os resultados.<br/> |



 

## <a name="remarks"></a>Comentários

Para evitar vazamentos de memória, você deve liberar os recursos para *pastrWords*, *pastrLines* e *pastrParagraphs*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




