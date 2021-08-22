---
title: Método CanPersist IWMDRMLicense (Wmdrmsdk.h)
description: O método CanPersist consulta se a licença pode ser persistida em um armazenamento de licenças local.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Formato de mídia do windows do método CanPersist
- Formato de mídia do windows do método CanPersist, interface IWMDRMLicense
- Formato de mídia da interface IWMDRMLicense , método CanPersist
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e174f0b7d48684e40cc5796d2ae95ec1bcaca99216c493c73609323daf276b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701214"
---
# <a name="iwmdrmlicensecanpersist-method"></a>Método IWMDRMLicense::CanPersist

O **método CanPersist** consulta se a licença pode ser persistida em um armazenamento de licenças local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfCanPersist* \[ out\]
</dt> <dd>

TRUE indica que a licença pode ser persistida.

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

[**IWMDRMLicense Interface**](iwmdrmlicense.md)
</dt> </dl>

 

 





