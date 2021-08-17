---
title: Método CreateDecryptor IWMDRMLicense (Wmdrmsdk.h)
description: O método CreateDecryptor cria um objeto descriptografador usando as configurações da licença atual.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Formato de mídia do windows do método CreateDecryptor
- Formato de mídia do windows do método CreateDecryptor, interface IWMDRMLicense
- Formato de mídia da interface IWMDRMLicense, método CreateDecryptor
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
ms.openlocfilehash: 03ac7e6bb1e9d4f9e5e7c706c0a9e3518f62b1068ed743dc795554dd43ac61e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027704"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>Método IWMDRMLicense::CreateDecryptor

O **método CreateDecryptor** cria um objeto descriptografador usando as configurações da licença atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDecryptor* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) do objeto recém-criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV MUITO \_ \_ PEQUENO**</dt> </dl> | Uma lista de revogação de conteúdo atualizada é necessária.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O método foi bem-sucedido.<br/>                         |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Createencryptor**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**IWMDRMLicense Interface**](iwmdrmlicense.md)
</dt> </dl>

 

 





