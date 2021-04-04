---
title: Mensagem de MCIWNDM_GETPOSITION (VFW. h)
description: A \_ mensagem GETPOSITION MCIWNDM recupera o valor numérico da posição atual dentro do conteúdo do dispositivo MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETPOSITION
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
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824218"
---
# <a name="mciwndm_getposition-message"></a>\_Mensagem GETPOSITION MCIWNDM

A **mensagem \_ GetPosition MCIWNDM** recupera o valor numérico da posição atual dentro do conteúdo do dispositivo MCI. Essa macro também fornece a posição atual no formulário de cadeia de caracteres em um buffer definido pelo aplicativo. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) ou [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .


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

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo usado para retornar a posição. Use zero para inibir a recuperação da posição como uma cadeia de caracteres. Se o dispositivo oferecer suporte a faixas, as informações de posição da cadeia de caracteres serão retornadas no formato TT: MM: SS: FF, em que TT corresponde a faixas, MM e SS correspondem a minutos e segundos, e FF corresponde a quadros.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro correspondente à posição atual. As unidades para o valor de posição dependem do formato de hora atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





