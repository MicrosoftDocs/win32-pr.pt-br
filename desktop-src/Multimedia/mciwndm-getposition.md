---
title: MCIWNDM_GETPOSITION mensagem (Vfw.h)
description: A mensagem GETPOSITION MCIWNDM recupera o valor numérico da posição atual dentro do \_ conteúdo do dispositivo MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83cf16f5945bfccbfd2f745ba22fac750f0536696aa2c4c06c2872bd318b263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525426"
---
# <a name="mciwndm_getposition-message"></a>Mensagem GETPOSITION MCIWNDM \_

A **mensagem \_ GETPOSITION MCIWNDM** recupera o valor numérico da posição atual dentro do conteúdo do dispositivo MCI. Essa macro também fornece a posição atual no formato de cadeia de caracteres em um buffer definido pelo aplicativo. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) ou [**MCIWndGetPositionString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamanho, em bytes, do buffer. Se a cadeia de caracteres terminada em nulo for maior que o buffer, ela será truncada. Use zero para inibir a recuperação da posição como uma cadeia de caracteres.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo usado para retornar a posição. Use zero para inibir a recuperação da posição como uma cadeia de caracteres. Se o dispositivo dá suporte a faixas, as informações de posição da cadeia de caracteres são retornadas no formato TT:MM:SS:FF em que TT corresponde a faixas, MM e SS correspondem a minutos e segundos e FF corresponde a quadros.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro correspondente à posição atual. As unidades para o valor de posição dependem do formato de hora atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





