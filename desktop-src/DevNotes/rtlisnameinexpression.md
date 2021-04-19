---
description: Determina se uma cadeia de caracteres Unicode corresponde ao padrão especificado.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: Função RtlIsNameInExpression
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755274"
---
# <a name="rtlisnameinexpression-function"></a>Função RtlIsNameInExpression

Determina se uma cadeia de caracteres Unicode corresponde ao padrão especificado.

## <a name="syntax"></a>Sintaxe


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Expressão* \[ de no\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres de padrão. Essa cadeia de caracteres pode conter caracteres curinga. Se o parâmetro *IgnoreCase* for true, a cadeia de caracteres deverá conter apenas caracteres maiúsculos.

</dd> <dt>

*Nome* \[ do no\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres a ser comparado com o padrão. Esta cadeia de caracteres não pode conter caracteres curinga.

</dd> <dt>

*IgnoreCase* \[ no\]
</dt> <dd>

**True** para correspondência que não diferencia maiúsculas de minúsculas ou **false** para correspondência que diferencia maiúsculas de minúsculas.

</dd> <dt>

*Upcase* \[ em, opcional\]
</dt> <dd>

Um ponteiro opcional para uma tabela de caracteres maiúsculos a ser usado para correspondência que não diferencia maiúsculas de minúsculas. Se esse parâmetro for NULL, a tabela de caracteres maiúsculos do sistema padrão será usada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a cadeia de caracteres corresponder ao padrão. Se a cadeia de caracteres não corresponder ao padrão, essa função retornará **false**.

## <a name="remarks"></a>Comentários

Esta função não tem nenhum arquivo de cabeçalho associado. A biblioteca de importação associada, ntdll. lib, está disponível no Microsoft Windows Driver Kit (WDK). Você também pode chamar essa função usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                              |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
