---
title: Método IWMDRMEncryptScatter InitEncryptScatter (Wmdrmsdk.h)
description: O método InitEncryptScatter inicializa a interface IWMDRMEncryptScatter para uso.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Formato de mídia do windows do método InitEncryptScatter
- Formato de mídia do windows do método InitEncryptScatter, interface IWMDRMEncryptScatter
- Formato de mídia da interface IWMDRMEncryptScatter , método InitEncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e83cce80b218d4cc8482d013537b7fae562312f242bc3549f4fa5069b1c677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027753"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>Método IWMDRMEncryptScatter::InitEncryptScatter

O **método InitEncryptScatter** inicializa a interface **IWMDRMEncryptScatter** para uso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cStreams* \[ Em\]
</dt> <dd>

Número de elementos na matriz *rgInfos.* Esse também é o número de fluxos incluídos nos dados a serem criptografados.

</dd> <dt>

*rgInfos* \[ Em\]
</dt> <dd>

Matriz de uma ou mais [**estruturas WMDRM \_ ENCRYPT SCATTER \_ \_ INFO.**](wmdrm-encrypt-scatter-info.md) Cada elemento contém informações de criptografia para um fluxo. O número de elementos nessa matriz deve ser igual ao valor *de cStreams*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**IWMDRMEncryptScatter Interface**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





