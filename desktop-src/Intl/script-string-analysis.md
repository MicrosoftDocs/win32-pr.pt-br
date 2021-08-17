---
description: Define alguns ou todos os atributos de caractere, glifos, larguras de avanço, posições x e y, mapeamentos de caractere para glifo e assim por diante, para uma cadeia de caracteres.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9481c641f182015d7a318c21c490f45fcc934e0df1baa52483707628eb4daa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390295"
---
# <a name="script_string_analysis"></a>ANÁLISE DE \_ CADEIA DE \_ CARACTERES DE SCRIPT

Define alguns ou todos os atributos de caractere, glifos, larguras de avanço, posições x e y, mapeamentos de caractere para glifo e assim por diante, para uma cadeia de caracteres.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Comentários

Essa é uma estrutura opaca alocada dinamicamente e recuperada por [**ScriptStringAnalyse.**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) Ele também é necessário para todas as outras funções **ScriptString. \***

Como a análise pode ser grande, é importante que seu aplicativo chame [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) assim que terminar com a cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Redistribuível<br/>          | Internet Explorer 5 ou posterior emWindows Me/98/95<br/>                         |
| Cabeçalho<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Estruturas Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**Scriptstringanalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




