---
title: Método IWMDRMSecurity GetRevocationDataVersion (wmdrmsdk. h)
description: O método GetRevocationDataVersion recupera o número de versão de uma lista de certificados revogados no repositório local.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Formato de mídia do Windows do método GetRevocationDataVersion
- Método GetRevocationDataVersion Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetRevocationDataVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754694"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>Método IWMDRMSecurity:: GetRevocationDataVersion

O método **GetRevocationDataVersion** recupera o número de versão de uma lista de certificados revogados no repositório local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*f \_ guidRevocationType* \[ em\]
</dt> <dd>

GUID que especifica o tipo de lista de revogação. Defina como uma das constantes na tabela a seguir.



| Constante de GUID                 | Descrição                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_aplicativo WMDRM RErevocationtype \_    | Especifica a lista de certificados revogados do aplicativo.                           |
| \_dispositivo WMDRM RErevocationtype \_ | Especifica a lista de certificados revogados do dispositivo.                                |
| WMDRM \_ RErevocationtype \_ CARDEA | Especifica a lista de revogação de certificados do Windows Media DRM para dispositivos de rede. |



 

</dd> <dt>

saída de *f \_ pdwCRLVersion* \[\]
</dt> <dd>

Variável que recebe o número de versão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Revogação e renovação de componentes automatizados**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





