---
title: Método Decrypt IWMSecureBuffer (wmdrmsdk. h)
description: O método Decrypt descriptografa um ponteiro de dados que foi criptografado chamando o método Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Método Decrypt Windows Media Format
- Método Decrypt Windows Media Format, interface IWMSecureBuffer
- IWMSecureBuffer interface formato Windows Media, método Decrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9867cb6476ab0a2838903c906f662032e14dfb0d4fa0547b045672e03b6ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930096"
---
# <a name="iwmsecurebufferdecrypt-method"></a>IWMSecureBuffer: método ecrypt de:D

O método **Decrypt** descriptografa um ponteiro de dados que foi criptografado chamando o método [**Encrypt**](iwmsecurebuffer-encrypt.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSecureChannel* \[ no\]
</dt> <dd>

Ponteiro para uma interface de canal segura que contém o ponteiro de dados criptografados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Encrypt**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**Interface IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 





