---
description: Função de proxy para o método getdatapointr.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: Função IWICBitmapLock_GetDataPointer_STA_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759818"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a>\_Função de proxy IWICBitmapLock Getdatapointr \_ STA \_

Função de proxy para o método [**Getdatapointr**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Isso \_ PTR* \[\]
</dt> <dd>

Tipo: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _

Ponteiro para este objeto [_ *IWICBitmapLock* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

</dd> <dt>

*pcbBufferSize* \[ fora\]
</dt> <dd>

Tipo: **uint \** _

Um ponteiro que recebe o tamanho do buffer.

</dd> <dt>

_ppbData * \[ out\]
</dt> <dd>

Tipo: **byte \* \***

Um ponteiro que recebe um ponteiro para o pixel superior esquerdo no retângulo bloqueado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




