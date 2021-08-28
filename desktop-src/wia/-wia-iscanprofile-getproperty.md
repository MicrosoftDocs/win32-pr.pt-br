---
description: Obtém o valor das propriedades filho especificadas no <Properties> elemento de um perfil de verificação.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'Método IScanProfile:: GetProperty (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: ef09115c7131df21697540fa941f8bd863650bc029601088b4a0f8c80e9b1a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814076"
---
# <a name="iscanprofilegetproperty-method"></a>Método IScanProfile:: GetProperty

Obtém o valor das propriedades filho especificadas no `<Properties>` elemento de um perfil de verificação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*número* \[ de no\]
</dt> <dd>

Tipo: **ULONG**

O número de entradas nas matrizes que são apontadas por *pid* e *pvar*.

</dd> <dt>

*pid* \[ no\]
</dt> <dd>

Tipo: **Propid \***

Um ponteiro para uma matriz dos números de identificação das propriedades a serem definidas. Cada valor na matriz é uma [constante de propriedade WIA](-wia-wia-property-constants.md).

</dd> <dt>

*pvar* \[ fora\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Um ponteiro para uma matriz de valores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Retornará S \_ false se qualquer um dos valores de propriedade não estiver disponível; caso contrário, retornará S \_ OK ou um código de erro com padrão.

## <a name="remarks"></a>Comentários

O tipo de cada valor deve ser do mesmo tipo que foi definido com a chamada para [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).

Cada valor na matriz que *pid* aponta para é uma das constantes da [Propriedade WIA](-wia-wia-property-constants.md). Você pode estender esse sistema de identificação. Consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>ScanProfile. h</dt> </dl>    |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> <dt>

[Constantes da propriedade WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definindo propriedades personalizadas](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
