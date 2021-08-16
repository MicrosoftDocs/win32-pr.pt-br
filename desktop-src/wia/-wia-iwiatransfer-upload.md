---
description: Inicia um carregamento de dados de um único item do chamador.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'método IWiaTransfer:: Upload (Wia. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66bd542d27f29aa8fd531b6f3d8089d296efe2d963bcf967a0c1ab07e6f0db8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208234"
---
# <a name="iwiatransferupload-method"></a>método IWiaTransfer:: Upload

Inicia um carregamento de dados de um único item do chamador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*pSource* \[ no\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Especifica um ponteiro para os dados de [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> <dt>

*pIWiaTransferCallback* \[ no\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Especifica um ponteiro para a interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) do chamador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
