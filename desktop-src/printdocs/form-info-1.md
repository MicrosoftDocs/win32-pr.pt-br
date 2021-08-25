---
description: A FORM_INFO_1 contém informações sobre um formulário de impressão. As informações incluem a origem dos formulários de impressão, seu nome, suas dimensões e as dimensões de sua área imprimível.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: FORM_INFO_1 (Winspool.h)
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
ms.openlocfilehash: b6f620d8bd2ed4ef39fc868c91068e10a7ff43f57d98510ecfbae1dbe2ae7c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949256"
---
# <a name="form_info_1-structure"></a>FORM_INFO_1 estrutura

A **FORM_INFO_1** contém informações sobre um formulário de impressão. As informações incluem a origem do formulário de impressão, seu nome, suas dimensões e as dimensões de sua área imprimível.

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
| FORM_USER    | Se esse sinalizador de bit estiver definido, o formulário será definido pelo usuário. Formulários com esse conjunto de sinalizadores são definidos no Registro.        |
| FORM_BUILTIN | Se esse sinalizador de bit estiver definido, o formulário faz parte do spooler. As definições de formulário com esse sinalizador definido não aparecem no Registro. |
| FORM_PRINTER | Se esse sinalizador de bit estiver definido, o formulário será associado a uma determinada impressora e sua definição aparecerá no Registro.          |



 

</dd> <dt>

**Pname**
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
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **_FORM_INFO_1W** (Unicode) **e _FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




