---
title: Método createencryptr IWMDRMLicense (wmdrmsdk. h)
description: O método createencryptr cria um objeto de criptografador usando as configurações da licença atual.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Método createencryptr formato de mídia do Windows
- Método createencryptr formato de mídia do Windows, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método createencryptr
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481e33b6a3d4ffff3805ccc14f45b06a12ad2296fdaaedf13608f3a519c6ed10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433655"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>Método IWMDRMLicense:: createencryptr

O método **Createencryptr** cria um objeto de criptografador usando as configurações da licença atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEncryptor* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IWMDRMEncrypt**](iwmdrmencrypt.md) do objeto recém-criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt> </dl> | Uma lista de revogação de conteúdo atualizada é necessária.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O método foi bem-sucedido.<br/>                         |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Createdescriptografar**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





