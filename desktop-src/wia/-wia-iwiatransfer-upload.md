---
description: Inicia um carregamento de dados de um único item do chamador.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'Método IWiaTransfer:: upload (WIA. h)'
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
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164529"
---
# <a name="iwiatransferupload-method"></a>Método IWiaTransfer:: upload

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

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Especifica um ponteiro para os dados de [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> <dt>

_pIWiaTransferCallback * \[ in\]
</dt> <dd>

Tipo: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Especifica um ponteiro para a interface [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) do chamador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
