---
description: Exclui o perfil de exame especificado.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: 'IScanProfileMgr: método eleteProfile de:D (Scanprofilemgr. h)'
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
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921803"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>IScanProfileMgr: método eleteProfile de:D

Exclui o perfil de exame especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pScanProfile* \[ no\]
</dt> <dd>

Tipo: **[**IScanProfile**](-wia-iscanprofile.md) \** _

Um ponteiro para o perfil.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

**IScanProfileMgr::D eleteprofile** exclui o perfil do disco e destrói o objeto de perfil na memória.

Use o método [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) quando mais de um objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) puderem criar ou excluir perfis ao mesmo tempo.

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

 

 




