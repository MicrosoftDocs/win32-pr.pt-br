---
description: Define o nome amigável do perfil.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'Método IScanProfile:: SetName (ScanProfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 0023353f298d5b6690345d559517c3840d33da6eb836c983b85924b5c4ac4260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441467"
---
# <a name="iscanprofilesetname-method"></a>Método IScanProfile:: SetName

Define o nome amigável do perfil.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrname* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O nome amigável do perfil.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é necessário porque o GUID de um perfil não pode ser usado para exibir o perfil de verificação para um usuário.

Um usuário pode alterar o nome amigável de um perfil com o método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

As alterações em um perfil não são salvas no disco até que o aplicativo chame o método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .

Se dois aplicativos criarem objetos de perfil de verificação do mesmo arquivo XML e cada aplicativo gravar alterações em seu objeto, somente as alterações feitas pelo aplicativo que chama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last serão salvas no disco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>ScanProfile. h</dt> </dl>    |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



 

 




