---
title: Método IWMDRMEncryptScatter InitEncryptScatter (wmdrmsdk. h)
description: O método InitEncryptScatter Inicializa a interface IWMDRMEncryptScatter para uso.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Formato de mídia do Windows do método InitEncryptScatter
- Método InitEncryptScatter Windows Media Format, interface IWMDRMEncryptScatter
- Formato de mídia do Windows de interface IWMDRMEncryptScatter, método InitEncryptScatter
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
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753624"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>Método IWMDRMEncryptScatter:: InitEncryptScatter

O método **InitEncryptScatter** Inicializa a interface **IWMDRMEncryptScatter** para uso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cStreams* \[ no\]
</dt> <dd>

Número de elementos na matriz *rgInfos* . Esse também é o número de fluxos incluídos nos dados a serem criptografados.

</dd> <dt>

*rgInfos* \[ no\]
</dt> <dd>

Matriz de uma ou mais estruturas de [**\_ \_ \_ informações de dispersão de WMDRM Encrypt**](wmdrm-encrypt-scatter-info.md) . Cada elemento contém informações de criptografia para um fluxo. O número de elementos nesta matriz deve ser igual ao valor de *cStreams*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**Interface IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





