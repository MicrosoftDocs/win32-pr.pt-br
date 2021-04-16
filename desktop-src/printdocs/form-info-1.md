---
description: A estrutura de FORM_INFO_1 contém informações sobre um formulário de impressão. As informações incluem a origem dos formulários de impressão, seu nome, suas dimensões e as dimensões de sua área imprimível.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Estrutura de FORM_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772726"
---
# <a name="form_info_1-structure"></a>Estrutura de FORM_INFO_1

A estrutura de **FORM_INFO_1** contém informações sobre um formulário de impressão. As informações incluem a origem do formulário de impressão, seu nome, suas dimensões e as dimensões de sua área imprimível.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**Sinalizadores**
</dt> <dd>

As propriedades do formulário. Os valores a seguir são definidos.



| Valor         | Significado                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| FORM_USER    | Se esse sinalizador de bit for definido, o formulário terá sido definido pelo usuário. Formulários com esse sinalizador definido são definidos no registro.        |
| FORM_BUILTIN | Se esse sinalizador de bit estiver definido, o formulário será parte do spooler. As definições de formulário com este sinalizador definido não aparecem no registro. |
| FORM_PRINTER | Se esse sinalizador de bit for definido, o formulário será associado a uma determinada impressora e sua definição aparecerá no registro.          |



 

</dd> <dt>

**pName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do formulário. O nome do formulário não pode exceder 31 caracteres.

</dd> <dt>

**Tamanho**
</dt> <dd>

A largura e a altura, em milésimos de milímetros, do formulário.

</dd> <dt>

**ImageableArea**
</dt> <dd>

A largura e a altura, em milésimos de milímetros, do formulário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **_FORM_INFO_1W** (Unicode) e **_FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddFormat**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**Formulário**](setform.md)
</dt> </dl>

 

 




