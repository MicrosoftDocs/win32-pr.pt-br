---
description: Retorna uma cadeia de caracteres que contém o nome do dispositivo de tablet.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: Método ITablet::GetName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 089bebc48fce9c720933f829ab83d04bf24fac3d8e2678369865cf2fe58650f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350675"
---
# <a name="itabletgetname-method"></a>Método ITablet::GetName

Retorna uma cadeia de caracteres que contém o nome do dispositivo de tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppwszName* \[ out\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de tablet.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

É responsabilidade do chamador liberar a memória retornada desse método usando [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITablet Interface**](itablet.md)
</dt> </dl>

 

