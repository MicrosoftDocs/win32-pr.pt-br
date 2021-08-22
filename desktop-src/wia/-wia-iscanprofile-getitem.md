---
description: Obtém o GUID da categoria do item WIA (Aquisição de Imagem Windows) 2.0 ao que o perfil está associado.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: Método IScanProfile::GetItem (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 5a7f52a2d89bbd35b59febb25528fe493c4b5646afc70251fc19978d6d6265db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451036"
---
# <a name="iscanprofilegetitem-method"></a>Método IScanProfile::GetItem

Obtém o GUID da categoria do item WIA (Aquisição de Imagem Windows) 2.0 ao que o perfil está associado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pguidCategory* \[ out\]
</dt> <dd>

Tipo: **\* GUID**

Um ponteiro para o GUID da categoria do item WIA 2.0. Essa é sempre uma das constantes DE CATEGORIA DE \_ ITEM IPA do \_ WIA. \_

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

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

[Esquema de perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




