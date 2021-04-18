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
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796210"
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

## <a name="return-value"></a>Retornar valor

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

 

 





