---
title: Método GetLicenseProperty IWMDRMLicense (Wmdrmsdk.h)
description: O método GetLicenseProperty recupera uma propriedade da licença atual.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Formato de mídia do windows do método GetLicenseProperty
- Formato de mídia do windows do método GetLicenseProperty, interface IWMDRMLicense
- Formato de mídia da interface IWMDRMLicense , método GetLicenseProperty
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167fc0aa050765700805b4339e68142fa5d1eb7fc99e010c7393095dd9aa5c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084836"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>Método IWMDRMLicense::GetLicenseProperty

O **método GetLicenseProperty** recupera uma propriedade da licença atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrName* \[ Em\]
</dt> <dd>

Nome da propriedade a ser recuperada. De acordo com uma das constantes na tabela a seguir:



| Constante                   | Descrição                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRMNet \_ Revocation | Use para obter a lista Windows DRM de Mídia para Dispositivos de Rede revogada para a licença atual.                        |
| g \_ wszWMDRM \_ SAPLEVEL      | Use para obter o nível sap (caminho de áudio seguro) necessário para reproduzir o conteúdo coberto pela licença atual.                |
| g \_ wszWMDRM \_ SAPRequired   | Use para verificar se a licença atual requer que o SAP seja usado para reproduzir o conteúdo.                               |
| g \_ wszWMDRM \_ SOURCEID      | Use para obter o identificador de origem da licença atual.                                                            |
| g \_ wszWMDRM \_ PRIORITY      | Use para obter a prioridade da licença atual. Licenças de prioridade mais alta são aplicadas antes de licenças de prioridade mais baixa. |
| g \_ wszWMDRM \_ UplinkID      | Use para obter a ID da chave da licença raiz na cadeia de licenças à que a licença atual pertence.                  |



 

</dd> <dt>

*ppropVariant* \[ out\]
</dt> <dd>

Recebe o valor da propriedade.

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
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Getlicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**IWMDRMLicense Interface**](iwmdrmlicense.md)
</dt> </dl>

 

 





