---
description: Procura um arquivo no cache Arquivos Offline que atenda aos critérios especificados.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: Função CSCFindFirstFileW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748694"
---
# <a name="cscfindfirstfilew-function"></a>Função CSCFindFirstFileW

\[Essa função não tem suporte e não deve ser usada.\]

Procura um arquivo no cache Arquivos Offline que atenda aos critérios especificados.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszFileName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um caminho ou diretório UNC válido.

</dd> <dt>

*lpFind32* \[ fora\]
</dt> <dd>

Um ponteiro para a estrutura de [**\_ \_ dados de localização do Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) que recebe informações sobre o arquivo ou subdiretório.

</dd> <dt>

*lpdwStatus* \[ fora\]
</dt> <dd>

Um código NTSTATUS que indica o status da chamada.

</dd> <dt>

*lpdwPinCount* \[ fora\]
</dt> <dd>

Esse parâmetro será diferente de zero se o arquivo tiver sido disponibilizado offline ou 0 caso contrário.

</dd> <dt>

*lpdwHintFlags* \[ fora\]
</dt> <dd>

Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                | Significado                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**Sinalizador \_ \_Usuário de \_ PIN \_ de dica de CSC**</dt> <dt></dt> </dl>                                | Um usuário tornou o arquivo disponível offline.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**Sinalizador \_ PIN de dica de CSC \_ \_ \_ herdar o \_ usuário**</dt> <dt>0x02</dt> </dl>       | Um usuário tornou o pai disponível offline e marcou o pai de modo que seus filhos estejam disponíveis offline.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**Sinalizador \_ O \_ PIN da dica de CSC \_ herda o \_ \_ sistema**</dt> <dt>0x04</dt> </dl> | Uma política de administrador ou de grupo tornou o pai disponível offline e marcou o pai de modo que seus filhos estejam disponíveis offline.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**Sinalizador \_ O \_ \_ \_ sistema de PIN de dica do CSC**</dt> <dt>0x10</dt> </dl>                          | Um administrador ou política de grupo disponibilizou o arquivo offline.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para receber as informações de data e hora do arquivo ou subdiretório.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um identificador de pesquisa usado em uma chamada subsequente para [**CSCFindNextFileW**](cscfindnextfilew.md) ou [**CSCFindClose**](cscfindclose.md).

Se a função falhar, o valor retornado será **INVALID\_HANDLE\_VALUE**.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
