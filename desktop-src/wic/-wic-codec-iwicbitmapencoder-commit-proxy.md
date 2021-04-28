---
description: Função IWICBitmapEncoder_Commit_Proxy function-proxy para o método Commit.
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: Função IWICBitmapEncoder_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 934b2e21097a671c2b52ea77ab07caf25ab521a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091184"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a>Função de proxy de \_ confirmação IWICBitmapEncoder \_

Função de proxy para o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Ponteiro para este objeto [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




