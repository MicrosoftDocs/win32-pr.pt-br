---
title: Mensagem de TB_ADDSTRING (commctrl. h)
description: Adiciona uma nova cadeia de caracteres ao pool de cadeias da barra de ferramentas.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- Controles de TB_ADDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755828"
---
# <a name="tb_addstring-message"></a>\_Mensagem de caracteres ADDSTRING TB

Adiciona uma nova cadeia de caracteres ao pool de cadeias da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Manipule a instância de módulo com um arquivo executável que contém o recurso de cadeia de caracteres. Se *lParam* apontar para uma matriz de caractere com uma ou mais cadeias de caracteres, defina esse parâmetro como **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de recurso para o recurso de cadeia de caracteres ou um ponteiro para uma matriz TCHAR. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice da primeira nova cadeia de caracteres se for bem-sucedida ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Se *wParam* for **NULL**, *lParam* apontará para uma matriz de caracteres com uma ou mais cadeias terminadas com nulo. A última cadeia de caracteres na matriz deve ser terminada com dois caracteres nulos.

Se *wParam* for o HINSTANCE do aplicativo ou de outro módulo que contém um recurso de cadeia de caracteres, *lParam* será o identificador de recurso da cadeia de caracteres. Cada item na cadeia de caracteres deve começar com um caractere separador arbitrário e a cadeia de caracteres deve terminar com dois caracteres. Por exemplo, o texto para três botões pode aparecer na tabela de cadeia de caracteres como "/New/Open/Save//". A mensagem retorna o índice de "New" no pool de cadeias de caracteres da barra de ferramentas e os outros itens estão em posições consecutivas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ ADDSTRINGW** (Unicode) e **TB \_ addstringa** (ANSI)<br/>                 |



 

 





