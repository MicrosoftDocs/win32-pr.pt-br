---
description: Contém informações sobre um formulário de impressão localizável.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: FORM_INFO_2 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: fd933bf0ace6f394a801ab8dc4ef1fa30344b47966c09865a3aa4b713c6f2ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971515"
---
# <a name="form_info_2-structure"></a>Estrutura FORM \_ INFO \_ 2

Contém informações sobre um formulário de impressão localizável.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**Sinalizadores**
</dt> <dd>

As propriedades do formulário. Os valores a seguir são definidos, mas apenas um pode ser definido. Quando o **FORM \_ INFO \_ 2** é retornado por [**GetForm**](getform.md) ou [**EnumForms,**](enumforms.md)os sinalizadores são **definidos** como o valor atual no banco de dados de formulários.



| Valor         | Significado                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORM \_ USER    | Se esse sinalizador de bit estiver definido, o formulário será definido pelo usuário. Formulários com esse conjunto de sinalizadores são definidos no Registro.                                                                                                                                                                    |
| FORM \_ BUILTIN | Se esse sinalizador de bit estiver definido, o formulário faz parte do spooler. As definições de formulário com esse sinalizador definido não aparecem no Registro. Formulários integrados não podem ser modificados, portanto, esse sinalizador não deve ser definido quando a estrutura é passada para [**AddForm**](addform.md) ou [**SetForm.**](setform.md) |
| IMPRESSORA \_ FORM | Se esse sinalizador de bit estiver definido, o formulário será associado a uma determinada impressora e sua definição aparecerá no Registro.                                                                                                                                                                      |



 

</dd> <dt>

**Pname**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do formulário. O nome do formulário não pode exceder 31 caracteres.

</dd> <dt>

**Tamanho**
</dt> <dd>

A largura e a altura do formulário em milésimos de milímetros.

</dd> <dt>

**ImageableArea**
</dt> <dd>

A largura e a altura, em milésimos de milímetros, da área da página na qual a impressora pode imprimir.

</dd> <dt>

**pKeyword**
</dt> <dd>

Um ponteiro para um identificador de cadeia de caracteres não localizável do formulário. Quando passado para [**AddForm**](addform.md) ou [**SetForm**](setform.md), isso fornece ao chamador um meio de identificar o formulário em todas as localidades.

</dd> <dt>

**StringType**
</dt> <dd>

Especifica como um nome de exibição localizado para o formulário é obtido em runtime. Os valores a seguir são definidos. Somente um pode ser definido em qualquer chamada para [**AddForm**](addform.md) ou [**SetForm.**](setform.md) TANTO STRING MUIDLL quanto STRING LANGPAIR podem ser definidos no \_ \_ FORM INFO **\_ \_ 2** (s) retornado por [**GetForm**](getform.md) [**ou EnumForms**](enumforms.md). Consulte Observações.



| Valor            | Significado                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STRING \_ NONE     | Não há nenhum nome de exibição localizado.                                                                                                                                                            |
| STRING \_ MUIDLL   | O nome de exibição é extraído [da DLL Interface de Usuário Multilíngue](/windows/desktop/Intl/mui-resource-management) recursos localizados especificados em **pMuiDll.** A ID está no **membro dwResourceId.** |
| STRING \_ LANGPAIR | O nome de exibição e a ID de idioma são fornecidos diretamente por **pDisplayName** e o idioma é especificado por **wLangId**.                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

A [Interface de Usuário Multilíngue](/windows/desktop/Intl/mui-resource-management) DLL de recurso localizada que contém o nome de exibição localizado.

</dd> <dt>

**dwResourceId**
</dt> <dd>

A ID do recurso do nome de exibição do formulário em **pMuiDll.**

</dd> <dt>

**pDisplayName**
</dt> <dd>

O nome de exibição do formulário no idioma especificado por **wLangId.**

</dd> <dt>

**wLangId**
</dt> <dd>

O idioma do **pDisplayName.**

</dd> </dl>

## <a name="remarks"></a>Comentários

Em uma chamada para [**AddForm**](addform.md) ou [**SetForm:**](setform.md)

-   Se **StringType** for STRING \_ NONE, **pMuiDll** e **pDisplayName** deverão ser **NULL** e **dwResourceId** e **wLangId** deverão ser 0.
-   Se **StringType** for STRING \_ MUIDLL, **pDisplayName** deverá ser **NULL** e **wLangId** deverá ser 0.
-   Se **StringType** for STRING \_ LANGPAIR, **pMuiDll** deverá ser **NULL** e **dwResourceId** deverá ser 0.

Para um **FORM \_ INFO \_ 2** retornado por uma chamada para [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md):

-   Se **StringType** for STRING \_ MUIDLL e STRING \_ LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId** e **wLangId** terão valores válidos.
-   Se **StringType** for apenas STRING \_ MUIDLL, **pMuiDll** e **dwResourceId** terão valores válidos. **pDisplayName** será **NULL** e **wLangId** será 0.
-   Se **StringType** for somente \_ STRING LANGPAIR, **pDisplayName** e **wLangId** terão valores válidos. **pMuiDll** será **NULL** e **dwResourceId** será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ FORM \_ INFO \_ 2W** (Unicode) e **\_ FORM INFO \_ \_ 2A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[Interface do Usuário Multilíngue](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

