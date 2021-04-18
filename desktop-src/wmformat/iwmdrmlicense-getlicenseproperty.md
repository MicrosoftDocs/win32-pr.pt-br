---
title: Método getlicenciadoproperty IWMDRMLicense (wmdrmsdk. h)
description: O método getlicenciadoproperty recupera uma propriedade da licença atual.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Método getlicenciadoproperty Windows Media Format
- Método getlicenciadoproperty Windows Media Format, interface IWMDRMLicense
- IWMDRMLicense interface formato Windows Media, método getlicenciadoproperty
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
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793274"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>Método IWMDRMLicense:: getlicenseproperty

O método **Getlicenciadoproperty** recupera uma propriedade da licença atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrname* \[ no\]
</dt> <dd>

Nome da propriedade a ser recuperada. Defina como uma das constantes na tabela a seguir:



| Constante                   | Descrição                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| \_wszWMDRMNet \_ revogação de g | Use para obter a lista de certificados do Windows Media DRM para dispositivos de rede para a licença atual.                        |
| g \_ wszWMDRM \_ SAPLEVEL      | Use para obter o nível de caminho de áudio seguro (SAP) necessário para reproduzir o conteúdo coberto pela licença atual.                |
| g \_ wszWMDRM \_ SAPRequired   | Use para verificar se a licença atual requer que o SAP seja usado para reproduzir o conteúdo.                               |
| \_fonte de wszWMDRM g \_      | Use para obter o identificador de origem para a licença atual.                                                            |
| \_prioridade g wszWMDRM \_      | Use para obter a prioridade da licença atual. As licenças de prioridade mais alta são aplicadas antes das licenças de prioridade mais baixa. |
| g \_ wszWMDRM \_ uplinkid      | Use para obter a ID de chave da licença raiz na cadeia de licença à qual a licença atual pertence.                  |



 

</dd> <dt>

*ppropVariant* \[ fora\]
</dt> <dd>

Recebe o valor da propriedade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





