---
title: Método Encrypt de IWMSecureBuffer (wmdrmsdk. h)
description: O método Encrypt criptografa um ponteiro de dados.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Método Encrypt Windows Media Format
- Método Encrypt Windows Media Format, interface IWMSecureBuffer
- Formato de mídia do Windows da interface IWMSecureBuffer, método Encrypt
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
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782415"
---
# <a name="iwmsecurebufferencrypt-method"></a>Método IWMSecureBuffer:: Encrypt

O método **Encrypt** criptografa um ponteiro de dados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSecureChannel* \[ no\]
</dt> <dd>

Ponteiro para uma interface de canal segura que contém o ponteiro de dados para criptografar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Use este método para criptografar ponteiros de dados para que eles possam ser enviados entre limites de DLL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Descriptografar**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**Interface IWMSecureBuffer**](iwmsecurebuffer.md)
</dt> </dl>

 

 





