---
description: Obtém o número de IDs de propriedade em um perfil.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'Método IScanProfile:: GetNumPropIDS (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: b8193259844732b708e56ba5fb191bd9ed7f9bf8fac27609c256b4df9cc7ccb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441468"
---
# <a name="iscanprofilegetnumpropids-method"></a>Método IScanProfile:: GetNumPropIDS

Obtém o número de IDs de propriedade em um perfil.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*número* \[ de fora\]
</dt> <dd>

Tipo: **ULONG \***

O número de IDs de propriedade no perfil.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>ScanProfile. h</dt> </dl>    |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




