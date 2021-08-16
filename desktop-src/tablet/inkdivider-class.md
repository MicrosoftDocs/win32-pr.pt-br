---
description: Representa a capacidade de analisar o layout de uma coleção de traços e dividi-los em texto e gráficos.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: Classe InkDivider (Msinkaut15. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: d7dd98aaef627bac6a26340464c14c4e46c07d6a23f32c2664651503b5d79014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220827"
---
# <a name="inkdivider-class"></a>Classe InkDivider

Representa a capacidade de analisar o layout de uma coleção de traços e dividi-los em texto e gráficos.

**InkDivider** tem estes tipos de membros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="interfaces"></a>Interfaces

A classe **InkDivider** define essas interfaces.



| Interface       | Descrição                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkDivider** | Esse objeto implementa a interface com do **IInkDivider** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **InkDivider** tem esses métodos.



| Método                              | Descrição                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dividir**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | Retorna um objeto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) que contém informações estruturais sobre os traços no objeto **InkDivider** .<br/> |



 

### <a name="properties"></a>Propriedades

A classe **InkDivider** tem essas propriedades.



| Propriedade                                                             | Tipo de acesso           | Descrição                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | Leitura/gravação<br/> | Obtém ou define a altura de manuscrito esperada em unidades HIMETRIC.<br/>                                                      |
| [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | Leitura/gravação<br/> | Obtém ou define o objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) usado para reconhecimento de manuscrito.<br/> |
| [**Traços**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | Leitura/gravação<br/> | Obtém ou define a coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contida pelo objeto **InkDivider** . <br/>     |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

O objeto **InkDivider** usa o layout dos traços, a ordem na qual os traços são adicionados, a direção na qual os traços são desenhados e outros fatores para executar a análise da tinta. A coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que o objeto **InkDivider** analisa está contida na propriedade [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) do objeto **InkDivider** . O objeto **InkDivider** analisa dinamicamente a coleção InkStrokes à medida que você adiciona ou exclui da coleção, mas não executa nenhuma modificação dos traços.

Os resultados da análise são retornados em um objeto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

O objeto **InkDivider** usa um objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) para dividir com mais precisão os traços e atribuir uma cadeia de caracteres de reconhecimento aos resultados.

> [!Note]  
> O objeto **InkDivider** usa as configurações de propriedade padrão do objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) .

 

Se você não atribuir um contexto de reconhecedor ao objeto **InkDivider** , o objeto **InkDivider** ainda analisará a tinta, mas dividirá os traços menos precisamente e não associará o texto aos resultados da divisão.

> [!Note]  
> A propriedade [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) deve ser definida antes da adição de traços à propriedade [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) . Depois que os traços tiverem sido adicionados ao objeto **InkDivider** , a propriedade **RecognizerContext** não poderá ser alterada.

 

Atualmente, o **InkDivider** não dá suporte a idiomas verticais. Para o objeto **InkDivider** reconhecer esses idiomas corretamente, o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para o idioma deve dar suporte à funcionalidade de entrada gratuita e os caracteres devem ser gravados da esquerda para a direita.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                               |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut15. h (também requer Msinkaut15 \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> <dt>

[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

