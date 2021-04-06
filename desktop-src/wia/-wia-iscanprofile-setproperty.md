---
description: Define o valor das propriedades filho especificadas no <Properties> elemento de um perfil de verificação.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'Método IScanProfile:: SetProperty (ScanProfile. h)'
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
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647488"
---
# <a name="iscanprofilesetproperty-method"></a>Método IScanProfile:: SetProperty

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

*número* \[ de no\]
</dt> <dd>

Tipo: **ULONG**

O número de entradas nas matrizes que são apontadas por *pid* e *pvar*.

</dd> <dt>

*pid* \[ no\]
</dt> <dd>

Tipo: **Propid \** _

Um ponteiro para uma matriz de números de identificação das propriedades a serem definidas. Cada valor na matriz é uma [constante de propriedade WIA](-wia-wia-property-constants.md).

</dd> <dt>

_pvar * \[ in\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Um ponteiro para uma matriz de valores a serem atribuídos às propriedades.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Cada valor na matriz que *pid* aponta para é uma das constantes da [Propriedade WIA](-wia-wia-property-constants.md). Você pode estender esse sistema de identificação. Consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md).

As alterações em um perfil não são salvas no disco até que o aplicativo chame o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .

Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo gravar alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last serão salvas no disco.

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

**Conceitua**
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> <dt>

[Constantes da propriedade WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definindo propriedades personalizadas](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
