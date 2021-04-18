---
title: Método createdescriptografar IWMDRMLicense (wmdrmsdk. h)
description: O método createdecryptr cria um objeto de descriptografia usando as configurações da licença atual.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Método createdescriptografar formato de mídia do Windows
- Método createdescriptografar formato de mídia do Windows, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método createdescriptografar
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755266"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>Método IWMDRMLicense:: createdecryptr

O método **Createdecryptr** cria um objeto de descriptografia usando as configurações da licença atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDecryptor* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) do objeto recém-criado.

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

[**Createcriptografer**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





