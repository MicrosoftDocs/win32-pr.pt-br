---
description: Cria um perfil de verificação vazio e o associa a um scanner ou a outro item de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'Método IScanProfileMgr:: CreateProfile (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461203"
---
# <a name="iscanprofilemgrcreateprofile-method"></a>Método IScanProfileMgr:: CreateProfile

Cria um perfil de verificação vazio e o associa a um scanner ou a outro item de aquisição de imagem do Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

A ID do dispositivo ou o item do WIA 2,0.

</dd> <dt>

*bstrname* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O nome amigável do novo perfil.

</dd> <dt>

*guidCategory* \[ no\]
</dt> <dd>

Tipo: **GUID**

O GUID da categoria do dispositivo ou do item WIA 2,0. Deve ser uma das \_ constantes da categoria de item IPA do WIA \_ \_ .

</dd> <dt>

*ppScanProfile* \[ fora\]
</dt> <dd>

Tipo: **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

O endereço de um ponteiro para o novo perfil.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

**IScanProfileMgr:: CreateProfile** associa o dispositivo especificado ao novo perfil de verificação.

**IScanProfileMgr:: CreateProfile** gera automaticamente um GUID para o novo perfil. Obtenha o GUID com [**GetGUID**](-wia-iscanprofile-getguid.md).

Use o método [**IScanProfileMgr:: Refresh**](-wia-iscanprofilemgr-refresh.md) quando mais de um objeto [**IScanProfileMgr**](-wia-iscanprofilemgr.md) puderem criar ou excluir perfis ao mesmo tempo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




