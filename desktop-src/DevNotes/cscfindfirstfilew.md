---
description: Pesquisa um arquivo no cache Arquivos Offline que atenda aos critérios especificados.
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
ms.openlocfilehash: 7289fb19a0062ce66212927bbe3e77c9e90c54ceb1980f83265000cc228e27ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833406"
---
# <a name="cscfindfirstfilew-function"></a>Função CSCFindFirstFileW

\[Não há suporte para essa função e não deve ser usada.\]

Pesquisa um arquivo no cache Arquivos Offline que atenda aos critérios especificados.

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

*lpszFileName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um caminho ou diretório UNC válido.

</dd> <dt>

*lpFind32* \[ out\]
</dt> <dd>

Um ponteiro para a [**estrutura WIN32 \_ FIND \_ DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) que recebe informações sobre o arquivo ou subdiretório.

</dd> <dt>

*lpdwStatus* \[ out\]
</dt> <dd>

Um código NTSTATUS que indica o status da chamada.

</dd> <dt>

*lpdwPinCount* \[ out\]
</dt> <dd>

Esse parâmetro será diferente de zero se o arquivo tiver sido disponibilizado offline ou 0 caso contrário.

</dd> <dt>

*lpdwHintFlags* \[ out\]
</dt> <dd>

Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                | Significado                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**SINALIZADOR \_ PIN DE USUÁRIO DE DICA CSC \_ \_ \_ 0X01**</dt> <dt></dt> </dl>                                | Um usuário tornou o arquivo disponível offline.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**SINALIZADOR \_ PIN DE DICA CSC \_ \_ \_ \_ HERDE A 0X02**</dt> <dt></dt> </dl>       | Um usuário tornou o pai disponível offline e marcou o pai de modo que seus filhos estão disponíveis offline.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**SINALIZADOR \_ PIN DE DICA CSC \_ \_ \_ \_ HERDE O SISTEMA**</dt> <dt>0X04</dt> </dl> | Uma política de administrador ou grupo tornou o pai disponível offline e marcou o pai de modo que seus filhos estão disponíveis offline.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**SINALIZADOR \_ Sistema de \_ PIN DE \_ DICA \_ CSC**</dt> <dt>0x10</dt> </dl>                          | Uma política de administrador ou grupo tornou o arquivo disponível offline.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ out\]
</dt> <dd>

Um ponteiro para uma [**estrutura FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para receber as informações de data e hora do arquivo ou subdiretório.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um alça de pesquisa usado em uma chamada subsequente para [**CSCFindNextFileW**](cscfindnextfilew.md) ou [**CSCFindClose.**](cscfindclose.md)

Se a função falhar, o valor retornado será **INVALID\_HANDLE\_VALUE**.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
