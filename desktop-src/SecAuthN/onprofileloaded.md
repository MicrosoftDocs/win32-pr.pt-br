---
description: Verifica se o perfil de usuário online está carregado.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Função OnProfileLoaded (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662133"
---
# <a name="onprofileloaded-function"></a>Função OnProfileLoaded

Verifica se o perfil de usuário online está carregado.

## <a name="syntax"></a>Sintaxe


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProviderHandle* \[ no\]
</dt> <dd>

O identificador do provedor.

</dd> <dt>

*UserToken* \[ no\]
</dt> <dd>

Token do usuário cujo perfil está sendo carregado ou descarregado.

</dd> <dt>

*Carregado* \[ no\]
</dt> <dd>

**True** se o perfil tiver sido carregado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, a função retornará o STATUS \_ êxito.

Se a função falhar, a função retornará um código de erro diferente de zero que é um erro específico do provedor para fins de diagnóstico.

## <a name="remarks"></a>Comentários

Essa função é chamada cada vez que a função [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) é chamada. Ele não está sincronizado com **LoadUserProfile**; ou seja, **LoadUserProfile** pode ter retornado e o perfil pode ter sido descarregado pela hora em que a função foi chamada. Essa função pode ser chamada mais de uma vez mesmo quando o perfil tiver sido carregado. O provedor de identidade não deve supor que uma chamada para essa função com *Loaded* igual a true será seguida por uma chamada com *Loaded* igual a false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

 
