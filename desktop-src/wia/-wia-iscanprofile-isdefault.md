---
description: Obtém um valor que indica se o perfil é o perfil de exame padrão de um dispositivo IWiaItem2 associado.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Método IScanProfile:: IsDefault (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921070"
---
# <a name="iscanprofileisdefault-method"></a>Método IScanProfile:: IsDefault

Obtém um valor que indica se o perfil é o perfil de exame padrão de um dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) associado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbDefault* \[ fora\]
</dt> <dd>

Tipo: **bool \** _

Um ponteiro para um _ * BOOL * *.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE**


</dt> <dd>

O perfil é o padrão.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FOR**


</dt> <dd>

O perfil não é o padrão.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

*pbDefault* será **true** se o perfil contiver um `<Default>` elemento. Será **false** se nenhum elemento desse tipo estiver presente. O elemento não tem valor.

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

 

 




