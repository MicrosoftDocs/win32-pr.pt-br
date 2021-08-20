---
description: Exclui o perfil de verificação especificado.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: Método IScanProfileMgr::D eleteProfile (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 52a4f2fc11e2a2cac1c3b3c547ee1b7a967a5441fc44cd2bb213bdbf681df8f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670249"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>Método IScanProfileMgr::D eleteProfile

Exclui o perfil de verificação especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pScanProfile* \[ Em\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\***

Um ponteiro para o perfil.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

**IScanProfileMgr::D eleteProfile** exclui o perfil do disco e destrói o objeto de perfil na memória.

Use o [**método IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) quando mais de um objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) pode estar criando ou excluindo perfis ao mesmo tempo.

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

 

 




