---
description: Obtém o perfil de exame padrão.
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: 'Método IScanProfileMgr:: GetDefaultProfile (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e058094fc29510d6e073abc0b05374403a2b5cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813627"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a>Método IScanProfileMgr:: GetDefaultProfile

Obtém o perfil de exame padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

A ID do dispositivo.

</dd> <dt>

*ppScanProfile* \[ fora\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

O endereço de um ponteiro para o perfil padrão do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O perfil padrão tem um `<Default>` elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




