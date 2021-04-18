---
description: Define um cache de métrica de fonte do Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751217"
---
# <a name="script_cache"></a>CACHE de SCRIPT \_

Define um cache de métrica de fonte do Uniscribe.


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a>Comentários

Esta é uma estrutura opaca. O aplicativo deve alocar e reter uma \_ variável de cache de script para cada estilo de caractere usado. A variável deve ser inicializada como **NULL**.

Muitas funções de script assumem uma combinação de um identificador de contexto de dispositivo de hardware e uma variável de cache de SCRIPT \_ . O Uniscribe primeiro tenta acessar dados de fonte usando a \_ variável de cache de script. Ele inspeciona apenas o contexto do dispositivo de hardware se os dados necessários ainda não estiverem em cache.

O identificador de contexto do dispositivo de hardware pode ser passado para o Uniscribe como **nulo**. Se os dados exigidos pelo Uniscribe já estiverem em cache, o contexto do dispositivo não será acessado e a operação continuará normalmente.

Se o contexto do dispositivo for passado como **nulo** e o Uniscribe precisar acessá-lo por qualquer motivo, o Uniscribe retornará o código de erro E \_ pendente. Esse código é retornado rapidamente, permitindo que o aplicativo Evite chamadas [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) demoradas.

## <a name="examples"></a>Exemplos

O exemplo a seguir aplica-se a todas as funções que usam uma variável de cache de SCRIPT \_ e um identificador opcional para um contexto de dispositivo de hardware.


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Cancelar](uniscribe.md)
</dt> <dt>

[Estruturas do Uniscribe](uniscribe-structures.md)
</dt> <dt>

[Cache](caching.md)
</dt> </dl>

 

 
