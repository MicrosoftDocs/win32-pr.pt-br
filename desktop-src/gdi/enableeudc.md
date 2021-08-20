---
description: Essa função habilita ou desabilita o suporte para EUDC (caracteres definidos pelo usuário final).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: Função EnableEUDC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 5767be62d23e992223500bf7192fc89efe04f03288280c73445378e083cc1613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699470"
---
# <a name="enableeudc-function"></a>Função EnableEUDC

Essa função habilita ou desabilita o suporte para EUDC (caracteres definidos pelo usuário final).

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnableEUDC* \[ no\]
</dt> <dd>

Booliano que é definido como **true** para habilitar EUDC e **false** para desabilitar Eudc.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Se o EUDC estiver desabilitado, tentar exibir caracteres EUDC resultará em glifos ausentes ou inválidos.

Durante várias sessões, essa função afeta apenas a sessão atual.

é recomendável que você use essa função com o Windows XP SP2 ou posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>GDI32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




