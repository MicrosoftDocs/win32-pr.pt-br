---
title: Método ResetEnumeration de IWMDRMLicense (Wmdrmsdk.h)
description: O método ResetEnumeration redefine a lista de licenças para seu estado original. A licença ativa se torna a primeira licença na lista.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Formato de mídia do windows do método ResetEnumeration
- Formato de mídia do método ResetEnumeration, interface IWMDRMLicense
- Formato de mídia da interface IWMDRMLicense, método ResetEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dda6de46a2ce96d1fec1abaaae56edcbc5b0d6a73e8ee13f038dba6b5577c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027684"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a>Método IWMDRMLicense::ResetEnumeration

O **método ResetEnumeration** redefine a lista de licenças para seu estado original. A licença ativa se torna a primeira licença na lista.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMLicense Interface**](iwmdrmlicense.md)
</dt> </dl>

 

 





