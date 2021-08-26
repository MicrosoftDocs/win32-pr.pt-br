---
title: Método IWMDRMLicenseManagement CreateLicenseEnumeration (wmdrmsdk. h)
description: O método CreateLicenseEnumeration cria um objeto de enumerador de licença com o qual você pode obter informações sobre licenças no repositório de licenças local.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Formato de mídia do Windows do método CreateLicenseEnumeration
- Método CreateLicenseEnumeration Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método CreateLicenseEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e442870961735d09c786a21ed1ea8be765e8f0c59b3f760278be9316daa0bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881076"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>Método IWMDRMLicenseManagement:: CreateLicenseEnumeration

O método **CreateLicenseEnumeration** cria um objeto de enumerador de licença com o qual você pode obter informações sobre licenças no repositório de licenças local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pLicenseFilter* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ filtro de licença WMDRM**](wmdrm-license-filter.md) que contém os parâmetros de filtragem para a lista de licenças no enumerador.

</dd> <dt>

*pEnumerator* \[ fora\]
</dt> <dd>

Ponteiro que recebe o endereço da interface [**IWMDRMLicense**](iwmdrmlicense.md) do objeto enumerador de licença recém-criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**RIV do NS \_ E \_ DRM \_ \_ muito \_ pequeno**</dt> </dl> | Uma lista de revogação de conteúdo atualizada é necessária.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O método foi bem-sucedido.<br/>                         |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Enumerando licenças no repositório de licenças local**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





