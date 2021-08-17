---
description: Converte uma cadeia de caracteres em um GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: Função GUIDFromString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: 38dd6d6365c3b306e63634fee02ac7add07b1bf262598efc88ffec2595e14c82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351056"
---
# <a name="guidfromstring-function"></a>Função GUIDFromString

\[o **GUIDFromString** está disponível por meio do Windows XP com Service Pack 2 (SP2) ou Windows Vista. Ele pode ser alterado ou indisponível nas versões subsequentes. Os aplicativos devem usar [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) ou [**falha em IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) no lugar dessa função.\]

Converte uma cadeia de caracteres em um GUID.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psz* \[ no\]
</dt> <dd>

Tipo: **LPCTSTR**

Um ponteiro para a cadeia de caracteres terminada em nulo a ser convertida. A cadeia de caracteres deve estar no seguinte formato:

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pGuid* \[ fora\]
</dt> <dd>

Tipo: **LPGUID**

Ponteiro para um buffer para receber o GUID quando esse método retorna.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **bool**

**True** se o GUID foi criado com êxito; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Essa função não é declarada em um cabeçalho ou exportada pelo nome de um arquivo .dll. Ele deve ser carregado de Shell32.dll como ordinal 703 para **GUIDFromStringA** e ordinal 704 para **GUIDFromStringW**.

Ele também pode ser acessado de Shlwapi.dll como ordinal 269 para **GUIDFromStringA** e ordinal 270 para **GUIDFromStringW**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **GUIDFromStringW** (Unicode) e **GUIDFromStringA** (ANSI)<br/>                |



 

 
