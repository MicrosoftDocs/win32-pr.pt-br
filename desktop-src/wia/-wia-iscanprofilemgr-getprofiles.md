---
description: Obtém todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'Método IScanProfileMgr:: getprofiles (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3f736c126d1f12282662f0d30c64e9ec99ae8324d3492e0560130c39ee38dc82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035541"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>Método IScanProfileMgr:: getprofiles

Obtém todos os perfis de verificação disponíveis para o usuário no sistema em que seu aplicativo está sendo executado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulNumProfiles* \[ entrada, saída\]
</dt> <dd>

Tipo: **ULONG \***

Quando passado, um ponteiro para o número máximo de perfis a serem retornados. Quando retornado, um ponteiro para o número de perfis retornado.

</dd> <dt>

*ppScanProfile* \[ fora\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

O endereço de uma matriz de ponteiros para perfis.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o número total de perfis disponíveis para o usuário for menor do que o valor passado para *pulNumProfiles*, então *pulNumProfiles* retornará esse total. Caso contrário, ele retorna o mesmo valor que foi passado para ele.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




