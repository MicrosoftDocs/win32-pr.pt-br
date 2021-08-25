---
title: Método Encrypt IWMSecureBuffer (Wmdrmsdk.h)
description: O método Encrypt criptografa um ponteiro de dados.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Criptografar o formato de mídia do windows do método
- Criptografar o formato de mídia do windows do método , interface IWMSecureBuffer
- Formato de mídia da interface IWMSecureBuffer, método Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e5badce8249e5d6b9d2460fec0e72ef4ca4b81f5b8ffa0d3edd83729f98bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808306"
---
# <a name="iwmsecurebufferencrypt-method"></a>Método IWMSecureBuffer::Encrypt

O **método Encrypt** criptografa um ponteiro de dados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSecureChannel* \[ Em\]
</dt> <dd>

Ponteiro para uma interface de canal seguro que contém o ponteiro de dados a ser criptografado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Use esse método para criptografar ponteiros de dados para que eles possam ser enviados entre limites de DLL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Descriptografar**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**IWMSecureBuffer Interface**](iwmsecurebuffer.md)
</dt> </dl>

 

 





