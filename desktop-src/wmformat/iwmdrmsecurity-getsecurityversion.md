---
title: Método IWMDRMSecurity GetSecurityVersion (wmdrmsdk. h)
description: O método GetSecurityVersion recupera a versão do subsistema DRM no computador cliente.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Formato de mídia do Windows do método GetSecurityVersion
- Método GetSecurityVersion Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetSecurityVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750876"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a>Método IWMDRMSecurity:: GetSecurityVersion

O método **GetSecurityVersion** recupera a versão do subsistema DRM no computador cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbstrVersion* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o número de versão do subsistema DRM.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O número de versão é expresso como uma cadeia de caracteres que consiste em quatro números separados por pontos. O primeiro número é o número de versão principal, que geralmente é definido como 2. O segundo número é o número de versão secundário, variando de 2 a 10. O terceiro número é sempre definido como 0. O quarto número é definido como 0 ou 1 e é um valor booliano que indica se o subsistema foi individualizado. Por exemplo, um número de versão de "2.4.0.1" indica a quarta versão secundária individual da segunda versão principal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





