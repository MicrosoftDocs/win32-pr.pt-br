---
title: Mensagem de CDM_SETDEFEXT (Commdlg. h)
description: Define a extensão de nome de arquivo padrão para uma caixa de diálogo abrir ou salvar como no estilo do Explorer.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- Caixas de diálogo de CDM_SETDEFEXT mensagem
topic_type:
- apiref
api_name:
- CDM_SETDEFEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bd5706e0bccf0b61c0737ef54d6e227e5593bc9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590853"
---
# <a name="cdm_setdefext-message"></a>\_Mensagem CDM SETDEFEXT

\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog). Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]

Define a extensão de nome de arquivo padrão para uma caixa de diálogo **abrir** ou **salvar como** no estilo do Explorer. A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a nova extensão de nome de arquivo. Não deve incluir o ponto (.).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

A macro correspondente é a seguinte:

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Commdlg. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**DA OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Biblioteca de caixa de diálogo comum](common-dialog-box-library.md)
</dt> </dl>

 

