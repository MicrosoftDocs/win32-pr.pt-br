---
title: Método IWMDRMLicenseManagement ProcessLicenseDeletionMessage (wmdrmsdk. h)
description: O método ProcessLicenseDeletion exclui uma licença que foi importada para o conteúdo originalmente protegido com outro sistema de proteção de conteúdo.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Formato de mídia do Windows do método ProcessLicenseDeletionMessage
- Método ProcessLicenseDeletionMessage Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método ProcessLicenseDeletionMessage
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369be95314ceaf3c4babce9dacd962fd3391d4f39f8988ef56f51fb3133aee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027584"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>IWMDRMLicenseManagement: método rocessLicenseDeletionMessage de:P

O método **ProcessLicenseDeletion** exclui uma licença que foi importada para o conteúdo originalmente protegido com outro sistema de proteção de conteúdo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeletionMessage* \[ no\]
</dt> <dd>

Mensagem que identifica a licença a ser excluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





