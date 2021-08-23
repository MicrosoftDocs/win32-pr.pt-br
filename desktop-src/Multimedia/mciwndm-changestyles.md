---
title: Mensagem de MCIWNDM_CHANGESTYLES (VFW. h)
description: A \_ mensagem MCIWNDM CHANGESTYLES altera os estilos usados pela janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- mensagem de MCIWNDM_CHANGESTYLES Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5525066f4c377cc093e1e7a0dedd4edf7463792c136214a519da9744917cbc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525506"
---
# <a name="mciwndm_changestyles-message"></a>\_Mensagem MCIWNDM CHANGESTYLES

A mensagem **MCIWNDM \_ CHANGESTYLES** altera os estilos usados pela janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*mascara*
</dt> <dd>

Máscara que identifica os estilos que podem ser alterados. Essa máscara é o operador OR de todos os estilos que terão permissão para alterar.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valor*
</dt> <dd>

Novas configurações de estilo para a janela. Especifique zero para esse parâmetro para desativar todos os estilos identificados na máscara. Para obter uma lista dos estilos disponíveis, consulte a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





