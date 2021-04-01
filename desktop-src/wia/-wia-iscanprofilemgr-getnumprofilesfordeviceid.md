---
description: Obtém o número de perfis de verificação para o dispositivo.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'Método IScanProfileMgr:: GetNumProfilesforDeviceID (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164707"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a>Método IScanProfileMgr:: GetNumProfilesforDeviceID

Obtém o número de perfis de verificação para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

A ID do dispositivo.

</dd> <dt>

*pulNumProfiles* \[ fora\]
</dt> <dd>

Tipo: **ULONG \** _

Um ponteiro para o número de perfis disponíveis para o dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

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

 

 




