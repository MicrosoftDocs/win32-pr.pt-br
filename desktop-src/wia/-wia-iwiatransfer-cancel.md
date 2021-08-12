---
description: Cancela a operação de transferência atual.
ms.assetid: 42c6b2c3-7b6a-45d2-a7ce-844e95fe277b
title: 'Método IWiaTransfer:: Cancel (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Cancel
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f7dd35b076597d76f3dc75c92a6cdd57169e8b92601d11f1038f4b9c9c2a6aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440359"
---
# <a name="iwiatransfercancel-method"></a>Método IWiaTransfer:: Cancel

Cancela a operação de transferência atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




