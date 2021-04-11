---
description: Contém informações sobre um formulário de impressão localizável.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Estrutura de FORM_INFO_2 (winspool. h)
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
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169341"
---
# <a name="form_info_2-structure"></a>Estrutura de informações de formulário \_ \_ 2

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

As propriedades do formulário. Os valores a seguir são definidos, mas apenas um pode ser definido. Quando o **formulário \_ informações \_ 2** é retornado por [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md), **flags** é definido como o valor atual no banco de dados de formulários.



| Valor         | Significado                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| usuário do formulário \_    | Se esse sinalizador de bit for definido, o formulário terá sido definido pelo usuário. Formulários com esse sinalizador definido são definidos no registro.                                                                                                                                                                    |
| FORMULÁRIO \_ interno | Se esse sinalizador de bit estiver definido, o formulário será parte do spooler. As definições de formulário com este sinalizador definido não aparecem no registro. Os formulários internos não podem ser modificados, portanto, esse sinalizador não deve ser definido quando a estrutura é passada para [**AddForm**](addform.md) ou [**setform**](setform.md). |
| impressora de formulário \_ | Se esse sinalizador de bit for definido, o formulário será associado a uma determinada impressora e sua definição aparecerá no registro.                                                                                                                                                                      |



 

</dd> <dt>

**pName**
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

Um ponteiro para um identificador de cadeia de caracteres não localizável do formulário. Quando passado para [**AddFormat**](addform.md) ou [**setform**](setform.md), isso fornece ao chamador um meio de identificar o formulário em todas as localidades.

</dd> <dt>

**StringType**
</dt> <dd>

Especifica como um nome de exibição localizado para o formulário é obtido em tempo de execução. Os valores a seguir são definidos. Apenas um pode ser definido em qualquer chamada fornecida para [**AddForm**](addform.md) ou [**setform**](setform.md). A cadeia de caracteres \_ MUIDLL e a cadeia de caracteres \_ LANGPAIR podem ser definidas no **formato \_ info \_ 2** (s) retornado por [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md). Consulte Observações.



| Valor            | Significado                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cadeia de caracteres \_ nenhum     | Não há nenhum nome de exibição localizado.                                                                                                                                                            |
| Cadeia de caracteres \_ MUIDLL   | O nome de exibição é extraído da DLL de recursos localizadas da [interface do usuário multilíngüe](/windows/desktop/Intl/mui-resource-management) especificada em **pMuiDll**. A ID está no membro **dwResourceId** . |
| Cadeia de caracteres \_ LANGPAIR | O nome de exibição e a ID de idioma são fornecidos diretamente pelo **pDisplayName** e o idioma é especificado por **wLangId**.                                                                       |



 

</dd> <dt>

**pMuiDll**
</dt> <dd>

A DLL de recurso localizada da [interface de usuário multilíngue](/windows/desktop/Intl/mui-resource-management) que contém o nome de exibição localizado.

</dd> <dt>

**dwResourceId**
</dt> <dd>

A ID de recurso do nome de exibição do formulário em **pMuiDll**.

</dd> <dt>

**pDisplayName**
</dt> <dd>

O nome de exibição do formulário no idioma especificado por **wLangId**.

</dd> <dt>

**wLangId**
</dt> <dd>

O idioma do **pDisplayName**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Em uma chamada para [**AddForm**](addform.md) ou [**setform**](setform.md):

-   Se **StringType** for String \_ None, **pMuiDll** e **PDisplayName** deverão ser **nulos** e **dwResourceId** e **wLangId** deverão ser 0.
-   Se **StringType** for cadeia \_ de caracteres MUIDLL, **pDisplayName** deverá ser **nulo** e **wLangId** deverá ser 0.
-   Se **StringType** for cadeia \_ de caracteres LANGPAIR, **pMuiDll** deverá ser **nulo** e **dwResourceId** deverá ser 0.

Para uma **informação de formulário \_ \_ 2** retornada por uma chamada para [**GetForm**](getform.md) ou [**EnumForms**](enumforms.md):

-   Se **StringType** for a cadeia \_ de caracteres MUIDLL e a cadeia de caracteres \_ LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId** e **wLangId** terão valores válidos.
-   Se **StringType** for String \_ MUIDLL somente, **pMuiDll** e **dwResourceId** terão valores válidos. **pDisplayName** será **NULL** e **wLangId** será 0.
-   Se **StringType** for String \_ LANGPAIR somente, **pDisplayName** e **wLangId** terão valores válidos. **pMuiDll** será **NULL** e **dwResourceId** será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de **\_ formulário \_ \_ 2W** (Unicode) e **\_ informações de formulário \_ \_ 2a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[Interface do Usuário Multilíngue](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[**AddFormat**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**Formulário**](setform.md)
</dt> </dl>

 

