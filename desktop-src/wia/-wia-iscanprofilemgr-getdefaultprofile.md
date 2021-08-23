---
description: Obtém o perfil de verificação padrão.
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: Método IScanProfileMgr::GetDefaultProfile (Scanprofilemgr.h)
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
ms.openlocfilehash: a496a2e606e389f8b2e1dfd7808d56e4360108a27ef66fbc0937ef1040514e44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549756"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a>Método IScanProfileMgr::GetDefaultProfile

Obtém o perfil de verificação padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeviceID* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

A ID do dispositivo.

</dd> <dt>

*ppScanProfile* \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

O endereço de um ponteiro para o perfil padrão do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O perfil padrão tem um `<Default>` elemento .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema de perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




