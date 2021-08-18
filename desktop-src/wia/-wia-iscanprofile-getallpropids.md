---
description: Obtém todas as IDs de propriedade disponíveis em um perfil.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: Método IScanProfile::GetAllPropIDs (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7fd54e3e1cd45c3631df9b069ddf3c2e897037efb2870d00946f0a002e12f145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965775"
---
# <a name="iscanprofilegetallpropids-method"></a>Método IScanProfile::GetAllPropIDs

Obtém todas as IDs de propriedade disponíveis em um perfil.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*num* \[ in, out\]
</dt> <dd>

Tipo: **ULONG \***

O número de IDs de propriedade solicitadas ou retornadas.

</dd> <dt>

*ppid* \[ out\]
</dt> <dd>

Tipo: **PROPID \***

Um ponteiro para uma matriz de IDs de propriedade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema de perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




