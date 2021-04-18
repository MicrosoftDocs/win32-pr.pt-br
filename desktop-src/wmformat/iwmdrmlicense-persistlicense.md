---
title: Método IWMDRMLicense PersistLicense (wmdrmsdk. h)
description: O método PersistLicense salva a licença atual do repositório temporário no armazenamento de licença local permanente.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Formato de mídia do Windows do método PersistLicense
- Método PersistLicense Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método PersistLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771549"
---
# <a name="iwmdrmlicensepersistlicense-method"></a>IWMDRMLicense: método ersistLicense de:P

O método **PersistLicense** salva a licença atual do repositório temporário no armazenamento de licença local permanente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se a licença atual não estiver no repositório temporário, esse método falhará.

Você pode chamar [**cancontinue**](iwmdrmlicense-canpersist.md) para consultar se a licença tem permissão para ser persistente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





