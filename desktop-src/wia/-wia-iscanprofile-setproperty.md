---
description: Define o valor das propriedades filho especificadas no <Properties> elemento de um perfil de verificação.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: Método IScanProfile::SetProperty (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: ba4c7aff5139f1230179299d80065f1b933a6cf2d01d4ca03c045ccbe142c3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441422"
---
# <a name="iscanprofilesetproperty-method"></a>Método IScanProfile::SetProperty

Define o valor das propriedades filho especificadas no `<Properties>` elemento de um perfil de verificação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*num* \[ Em\]
</dt> <dd>

Tipo: **ULONG**

O número de entradas nas matrizes que são apontadas por *pid* e *pvar*.

</dd> <dt>

*pid* \[ Em\]
</dt> <dd>

Tipo: **PROPID \***

Um ponteiro para uma matriz de números de identificação das propriedades a serem definidas. Cada valor na matriz é uma constante de [propriedade WIA](-wia-wia-property-constants.md).

</dd> <dt>

*pvar* \[ Em\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Um ponteiro para uma matriz de valores a serem atribuídos às propriedades.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Cada valor na matriz para *a qual o pid* aponta é uma das [Constantes de Propriedade wia](-wia-wia-property-constants.md). Você pode estender esse sistema de identificação. Consulte [Definindo propriedades personalizadas.](-wia-defining-custom-properties.md)

As alterações em um perfil não são salvas no disco até que o aplicativo chama o [**método IScanProfile::Save.**](-wia-iscanprofile-save.md)

Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo grava alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile::Save**](-wia-iscanprofile-save.md) last serão salvas no disco.

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

**Conceitual**
</dt> <dt>

[Esquema de perfil de verificação](-wia-scan-profile-schema.md)
</dt> <dt>

[Constantes de propriedade WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definindo propriedades personalizadas](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
