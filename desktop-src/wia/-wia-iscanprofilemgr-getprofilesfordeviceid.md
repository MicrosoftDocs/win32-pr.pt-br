---
description: Obtém todos os perfis de verificação associados a um dispositivo.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'Método IScanProfileMgr:: GetProfilesforDeviceID (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789348"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a>Método IScanProfileMgr:: GetProfilesforDeviceID

Obtém todos os perfis de verificação associados a um dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

A ID do dispositivo.

</dd> <dt>

*pulNumProfiles* \[ entrada, saída\]
</dt> <dd>

Tipo: **ULONG \** _

Quando passado, um ponteiro para o número máximo de perfis a serem retornados. Quando retornado, o ponteiro para o número de perfis retornado.

</dd> <dt>

_ppScanProfile * \[ out\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

O endereço de um ponteiro para uma matriz de perfis.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o número total de perfis associados ao dispositivo for menor do que o valor passado para *pulNumProfiles*, então *pulNumProfiles* retornará esse total. Caso contrário, ele retorna o mesmo valor que foi passado para ele.

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

 

 




