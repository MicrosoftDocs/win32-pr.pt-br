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
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788662"
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

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>ScanProfile. h</dt> </dl>    |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



 

 




