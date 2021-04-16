---
description: Obtém o GUID da categoria do item de aquisição de imagem do Windows (WIA) 2,0 ao qual o perfil está associado.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'Método IScanProfile:: GetItem (ScanProfile. h)'
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
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747715"
---
# <a name="iscanprofilegetitem-method"></a>Método IScanProfile:: GetItem

Obtém o GUID da categoria do item de aquisição de imagem do Windows (WIA) 2,0 ao qual o perfil está associado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pguidCategory* \[ fora\]
</dt> <dd>

Tipo: **GUID \** _

Um ponteiro para o GUID da categoria do item WIA 2,0. Essa é sempre uma das constantes da \_ categoria de item IPA do WIA \_ \_ .

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

 

 




