---
description: Adiciona uma cadeia de caracteres e dados extras a uma tabela.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: função pSetupStringTableAddStringEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750396"
---
# <a name="psetupstringtableaddstringex-function"></a>função pSetupStringTableAddStringEx

\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]

Adiciona uma cadeia de caracteres e dados extras a uma tabela.

## <a name="syntax"></a>Sintaxe


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*STRINGTABLE* \[ no\]
</dt> <dd>

Um ponteiro para a tabela de cadeia de caracteres.

</dd> <dt>

*Cadeia de caracteres* \[ no\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres a ser adicionada à tabela.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

O valor desse parâmetro pode ser `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .



| Valor                                                                                                                                                                                                                                             | Significado                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <dt>**STRTAB \_ 0x001 \_ diferencia maiúsculas de minúsculas**</dt> <dt></dt> </dl> | A cadeia de caracteres diferencia maiúsculas de minúsculas.<br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <dt>**STRTAB \_ NOVO \_ EXTRADATA**</dt> <dt>0x004</dt> </dl>    | Há dados extras.<br/>      |



 

</dd> <dt>

*ExtraData* \[ em, opcional\]
</dt> <dd>

Um ponteiro opcional para um objeto de dados extra.

</dd> <dt>

*ExtraDataSize* \[ em, opcional\]
</dt> <dd>

O tamanho dos dados adicionais.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
