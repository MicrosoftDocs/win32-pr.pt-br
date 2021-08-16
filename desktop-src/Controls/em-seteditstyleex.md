---
title: Mensagem de EM_SETEDITSTYLEEX (RichEdit. h)
description: Define os sinalizadores de estilo de edição estendida atuais.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- controles de Windows de mensagem de EM_SETEDITSTYLEEX
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b96a353b62dc3a31affd9e827ee803c481bcd806eaad9f8a5d0e9dd35388cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831217"
---
# <a name="em_seteditstyleex-message"></a>\_Mensagem em SETEDITSTYLEEX

Define os sinalizadores de estilo de edição estendida atuais.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica um ou mais sinalizadores de estilo de edição estendida. Para obter uma lista de valores possíveis, consulte em [**\_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Uma máscara que consiste em um ou mais dos valores *wParam* . Somente os valores especificados nesta máscara serão definidos ou apagados. Isso permite que um único sinalizador seja definido ou limpo sem a leitura dos Estados de sinalizador atuais.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o estado dos sinalizadores de estilo de edição estendida depois que a edição avançada tentou implementar as alterações de estilo de edição. Os sinalizadores de estilo de edição são um conjunto de sinalizadores que indicam o estilo de edição atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETEDITSTYLEEX**](em-geteditstyleex.md)
</dt> </dl>

 

