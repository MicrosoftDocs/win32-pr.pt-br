---
description: Remove uma lista especificada de propriedades filho no <Properties> elemento de um perfil de verificação.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'Método IScanProfile:: RemoveProperty (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090809"
---
# <a name="iscanprofileremoveproperty-method"></a>Método IScanProfile:: RemoveProperty

Remove uma lista especificada de propriedades filho no `<Properties>` elemento de um perfil de verificação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*número* \[ de no\]
</dt> <dd>

Tipo: **ULONG**

O número de entradas na matriz para as quais a *pid* aponta.

</dd> <dt>

*pid* \[ no\]
</dt> <dd>

Tipo: **Propid \** _

Um ponteiro para uma matriz de números de identificação das propriedades a serem excluídas. Cada uma é uma [constante de propriedade WIA](-wia-wia-property-constants.md).

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

 

 




