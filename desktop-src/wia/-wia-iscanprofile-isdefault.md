---
description: Obtém um valor que indica se o perfil é o perfil de verificação padrão de um dispositivo IWiaItem2 associado.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: Método IScanProfile::IsDefault (Scanprofile.h)
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
ms.openlocfilehash: 3f763286a6db8430514cd70bc05eb160935e0fdc7ae8b5c452e8c09a113c0af5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882406"
---
# <a name="iscanprofileisdefault-method"></a>Método IScanProfile::IsDefault

Obtém um valor que indica se o perfil é o perfil de verificação padrão de um [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) associado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbDefault* \[ out\]
</dt> <dd>

Tipo: **BOOL \***

Um ponteiro para um **BOOL.**

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Verdade**


</dt> <dd>

O perfil é o padrão.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False**


</dt> <dd>

O perfil não é o padrão.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

*pbDefault será* **TRUE se** o perfil contiver um elemento `<Default>` . Será **FALSE se** esse elemento não estiver presente. O elemento não tem nenhum valor.

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

 

 




