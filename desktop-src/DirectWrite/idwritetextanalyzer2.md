---
title: Interface IDWriteTextAnalyzer2
description: Analisa várias propriedades de texto para processamento de script complexo.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Gravação direta da interface IDWriteTextAnalyzer2
- Gravação direta da interface IDWriteTextAnalyzer2, descrita
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a76d4b4b7c2ef09f82834ed2e7f40ee89d2ab80bd0595db62790f38831b86fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075566"
---
# <a name="idwritetextanalyzer2-interface"></a>Interface IDWriteTextAnalyzer2

Analisa várias propriedades de texto para processamento de script complexo.

## <a name="members"></a>Membros

A interface **IDWriteTextAnalyzer2** herda de [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1). **IDWriteTextAnalyzer2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDWriteTextAnalyzer2** tem esses métodos.



| Método                                                                                    | Descrição                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**CheckTypographicFeature**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | Verifica se um recurso tipográfico está disponível para um glifo ou um conjunto de glifos.<br/> |
| [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | Retorna a matriz de transformação 2x3 para o respectivo ângulo para desenhar a execução de glifo.<br/> |
| [**GetTypographicFeatures**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | Retorna uma lista completa de recursos OpenType disponíveis para um script ou uma fonte.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

