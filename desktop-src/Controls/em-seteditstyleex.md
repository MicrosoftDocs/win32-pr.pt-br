---
title: Mensagem de EM_SETEDITSTYLEEX (RichEdit. h)
description: Define os sinalizadores de estilo de edição estendida atuais.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- Controles de EM_SETEDITSTYLEEX de mensagens do Windows
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
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918984"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o estado dos sinalizadores de estilo de edição estendida depois que a edição avançada tentou implementar as alterações de estilo de edição. Os sinalizadores de estilo de edição são um conjunto de sinalizadores que indicam o estilo de edição atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETEDITSTYLEEX**](em-geteditstyleex.md)
</dt> </dl>

 

