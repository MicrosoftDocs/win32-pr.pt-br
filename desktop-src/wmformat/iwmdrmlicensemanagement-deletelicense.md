---
title: Método IWMDRMLicenseManagement DeleteLicense (wmdrmsdk. h)
description: O método DeleteLicense remove uma licença do armazenamento de licença local temporário.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Formato de mídia do Windows do método DeleteLicense
- Método DeleteLicense Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método DeleteLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977f7eaef1d6c8a505ce55d7d1683d7c9f4dabff5e59df7d8845773eefdff696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707936"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>IWMDRMLicenseManagement: método eleteLicense de:D

O método **DeleteLicense** remove uma licença do armazenamento de licença local temporário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrKID* \[ no\]
</dt> <dd>

ID da chave (KID) da licença a ser excluída.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Sinalizadores de opção de exclusão de licença. Defina como um dos valores na tabela a seguir.



| Valor                                    | Descrição                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| licença de exclusão de WMDRM \_ \_ \_ imediatamente      | Especifica que a licença deve ser removida do repositório imediatamente.                                                                                                                              |
| \_exclusão \_ \_ \_ de marca de licença do WMDRM para \_ limpeza | Especifica que a licença deve ser marcada para exclusão, mas não deve ser removida da loja até que o método [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) seja chamado. |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | O método foi bem-sucedido.<br/>                                                                                    |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | A licença especificada não existe no repositório.<br/> - OU –<br/> O repositório não foi encontrado.<br/> |



 

## <a name="remarks"></a>Comentários

Para excluir licenças do armazenamento de licença local permanente, você deve usar a revogação de licença.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





