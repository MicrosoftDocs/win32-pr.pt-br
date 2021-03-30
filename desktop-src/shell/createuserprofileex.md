---
description: Cria um perfil de usuário para um usuário especificado.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: Função CreateUserProfileEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104968790"
---
# <a name="createuserprofileex-function"></a>Função CreateUserProfileEx

\[Essa função não está disponível no Windows Vista.\]

Cria um perfil de usuário para um usuário especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psid* \[ no\]
</dt> <dd>

Tipo: **PSID**

O SID do novo usuário.

</dd> <dt>

*lpUserName* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

Ponteiro para um buffer que contém o nome de usuário do novo usuário.

</dd> <dt>

*lpUserHive* \[ em, opcional\]
</dt> <dd>

Tipo: **LPCTSTR**

Ponteiro para um buffer que contém o [hive do registro](../sysinfo/registry-hives.md) a ser usado. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lpProfileDir* \[ out, opcional\]
</dt> <dd>

Tipo: **LPTSTR**

Ponteiro para um buffer que, quando essa função retorna, recebe o caminho do diretório de perfil do usuário. Este parâmetro pode ser **NULL**.

</dd> <dt>

*dwDirSize* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Tamanho do buffer especificado por *lpProfileDir*, em TCHARs.

</dd> <dt>

*bWin9xUpg* \[ no\]
</dt> <dd>

Tipo: **bool**

**True** se o perfil do usuário estiver sendo criado como parte de uma migração de perfil do Windows 9x; caso contrário, **false**.

Quando **true**, o perfil do usuário é configurado no diretório de perfil padrão — normalmente C: \\ Documents and Settings \\ *username*. Se esse diretório já existir, ele será usado. Se não tiver, ele será criado.

Se **for false**, o diretório de perfil padrão será criado se ele não existir. Se o diretório de perfil padrão já existir, um novo diretório será criado para esse perfil de usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **bool**

Retorna **true** se o novo perfil de usuário foi criado com êxito; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Essa função não é declarada nos cabeçalhos Software Development Kit (SDK) e não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular a Userenv.dll. A versão ANSI da função, **CreateUserProfileExA** , é referenciada de Userenv.dll como ordinal 153. A versão Unicode, **CreateUserProfileExW** , é referenciada como ordinal 154.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/>  | Windows XP<br/>                                                                  |
| DLL<br/>                    | <dl> <dt>Userenv.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/> | **CreateUserProfileExW** (Unicode) e **CreateUserProfileExA** (ANSI)<br/>      |



 

 
