---
description: Obtém todas as IDs de propriedade disponíveis em um perfil.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Método IScanProfile:: GetAllPropIDs (ScanProfile. h)'
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
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763968"
---
# <a name="iscanprofilegetallpropids-method"></a>Método IScanProfile:: GetAllPropIDs

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

*número* \[ de entrada, saída\]
</dt> <dd>

Tipo: **ULONG \** _

O número de IDs de propriedade solicitadas ou retornadas.

</dd> <dt>

_ppid * \[ out\]
</dt> <dd>

Tipo: **Propid \** _

Um ponteiro para uma matriz de IDs de propriedade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>ScanProfile. h</dt> </dl>    |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




