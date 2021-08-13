---
description: Libera uma chave, hash ou objeto de provedor.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: Função SslFreeObject (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7415ac31147f08bec038da5af57e8a4bc0cc4d2d3f39cb3b8391f42dfcff21b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906485"
---
# <a name="sslfreeobject-function"></a>Função SslFreeObject

A **função SslFreeObject** libera uma chave, hash ou objeto de provedor.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hObject* \[ Em\]
</dt> <dd>

O identificador do objeto a ser liberado.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                       | Descrição                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl>    | Um alça interno não é válido.<br/>  |
| <dl> <dt>**STATUS \_ HANDLE \_ INVÁLIDO**</dt> <dt>0xC0000008L</dt> </dl> | O alça fornecido não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




