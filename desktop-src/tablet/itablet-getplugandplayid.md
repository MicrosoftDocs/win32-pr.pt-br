---
description: Retorna uma cadeia de caracteres que contém a ID de Plug and Play para o dispositivo tablet.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'Método ITablet:: GetPlugAndPlayId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793721"
---
# <a name="itabletgetplugandplayid-method"></a>Método ITablet:: GetPlugAndPlayId

Retorna uma cadeia de caracteres que contém a ID de Plug and Play para o dispositivo tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppwszPPId* \[ fora\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém a ID de Plug and Play para o dispositivo tablet.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

É responsabilidade do chamador liberar a memória retornada desse método usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

