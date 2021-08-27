---
title: CDM_GETFILEPATH mensagem (Commdlg.h)
description: Recupera o caminho e o nome do arquivo selecionado em uma caixa de diálogo Abrir ou Salvar como no estilo Explorer.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- CDM_GETFILEPATH caixa de diálogo de mensagem
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ac18880ef62df1d228c006f0bc33fcf4932cbb976419ee29464e49828d8173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786329"
---
# <a name="cdm_getfilepath-message"></a>Mensagem \_ GETFILEPATH do CDM

\[Começando com Windows Vista,  as  caixas de diálogo Abrir e Salvar como comuns foram superadas pela caixa [de diálogo Item Comum](../shell/common-file-dialog.md). Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]

Recupera o caminho e o nome do arquivo selecionado em uma caixa de diálogo Abrir **ou** Salvar **como** no estilo Explorer. A caixa de diálogo deve ter sido criada com o **sinalizador OFN \_ EXPLORER;** caso contrário, a mensagem falhará.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tamanho, em caracteres, do buffer *lParam.* Para a versão ANSI, esse é o número de bytes; para a versão Unicode, esse é o número de caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que recebe o nome e o caminho do arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será o tamanho, em caracteres, do nome do arquivo e da cadeia de caracteres de caminho, incluindo o caractere NULL de terminação. Esse é o número de bytes ou caracteres copiados para o buffer ou o tamanho do buffer necessário se o buffer for muito pequeno.

Se ocorrer um erro, o valor de retorno será menor que zero.

## <a name="remarks"></a>Comentários

A macro correspondente é a seguinte:

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Getopenfilename**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**Getsavefilename**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**Openfilename**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Biblioteca de caixas de diálogo comuns](common-dialog-box-library.md)
</dt> </dl>

