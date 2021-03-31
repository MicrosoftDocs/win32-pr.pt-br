---
description: Libera um objeto de chave, hash ou provedor.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: Função SslFreeObject (Sslprovider. h)
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
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827934"
---
# <a name="sslfreeobject-function"></a>Função SslFreeObject

A função **SslFreeObject** libera um objeto de chave, hash ou provedor.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hObject* \[ no\]
</dt> <dd>

O identificador do objeto a ser liberado.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | Um identificador interno não é válido.<br/>  |
| <dl> <dt>**Status \_ do \_Identificador inválido**</dt> <dt>0xC0000008L</dt> </dl> | O identificador fornecido não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




