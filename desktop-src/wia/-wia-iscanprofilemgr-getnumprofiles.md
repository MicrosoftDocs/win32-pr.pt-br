---
description: Obtém o número de perfis de verificação criados para o usuário no sistema em que seu aplicativo está sendo executado.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'Método IScanProfileMgr:: GetNumProfiles (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771591"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a>Método IScanProfileMgr:: GetNumProfiles

Obtém o número de perfis de verificação criados para o usuário no sistema em que seu aplicativo está sendo executado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulNumProfiles* \[ fora\]
</dt> <dd>

Tipo: **ULONG \** _

Um ponteiro para o número de perfis criados para o usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

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

 

 




