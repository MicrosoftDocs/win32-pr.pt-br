---
title: Método ISoftKbd DestroySoftKeyboardWindow (Softkbdc.h)
description: O método ISoftKbd DestroySoftKeyboardWindow destrói uma janela de teclado suave.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Método DestroySoftKeyboardWindow Estrutura de Serviços de Texto
- Método DestroySoftKeyboardWindow Estrutura de Serviços de Texto , interface ISoftKbd
- Interface ISoftKbd Estrutura de Serviços de Texto , método DestroySoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f4e08a07c76f8b89809782f14d31e677417dbe18f20d6a817f3b1f234a01d12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877894"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a>Método ISoftKbd::D çãoSoftKeyboardWindow

O **método ISoftKbd::D ySoftKeyboardWindow** destrói uma janela de teclado suave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                | Descrição                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método remove uma janela de teclado suave criada anteriormente com uma chamada para [**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





