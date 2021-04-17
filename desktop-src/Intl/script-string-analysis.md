---
description: Define alguns ou todos os atributos de caractere, glifos, larguras avançadas, posições x e y, mapeamentos de caractere para glifo e assim por diante, para uma cadeia de caracteres.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748992"
---
# <a name="script_string_analysis"></a>\_análise de cadeia de script \_

Define alguns ou todos os atributos de caractere, glifos, larguras avançadas, posições x e y, mapeamentos de caractere para glifo e assim por diante, para uma cadeia de caracteres.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Comentários

Essa é uma estrutura opaca que é alocada dinamicamente e recuperada pelo [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse). Ele também é necessário para todas as outras funções **ScriptString \** _.

Como a análise pode ser grande, é importante que seu aplicativo chame [_ *ScriptStringFree* *](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) assim que terminar com a cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Redistribuível<br/>          | Internet Explorer 5 ou posterior no Windows me/98/95<br/>                         |
| parâmetro<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Cancelar](uniscribe.md)
</dt> <dt>

[Estruturas do Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




