---
description: Retorna o GUID do perfil.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: Método IScanProfile::GetGUID (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 37d383d5975957c45b2aa5a0c90350f794e6f20deb9a7bfbe73c9f2d42b2bca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441574"
---
# <a name="iscanprofilegetguid-method"></a>Método IScanProfile::GetGUID

Retorna o GUID do perfil.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*retVal* \[ out\]
</dt> <dd>

Tipo: **\* GUID**

Um ponteiro para o GUID do perfil.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O GUID de um perfil é gerado automaticamente quando o perfil é criado com [**CreateProfile.**](-wia-iscanprofilemgr-createprofile.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema de perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




