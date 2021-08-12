---
description: Obtém o resultado de uma ação assíncrona.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'Método IAsyncAction:: GetResults'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 62196c7f8ded67bed0ecdb3ea33420de54301bbd379615126ada158ea9e725ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561048"
---
# <a name="iasyncactiongetresults-method"></a>Método IAsyncAction:: GetResults

Obtém o resultado de uma ação assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResults();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Esse método sempre retorna **S \_ OK**.

## <a name="remarks"></a>Comentários

Chamar o método **GetResults** não terá efeito se a implementação atual tiver um tipo dinâmico de [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                    |
| parâmetro<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
