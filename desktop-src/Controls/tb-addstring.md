---
title: TB_ADDSTRING mensagem (Commctrl.h)
description: Adiciona uma nova cadeia de caracteres ao pool de cadeias de caracteres da barra de ferramentas.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING controles Windows mensagem
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
ms.openlocfilehash: c0556add41addb4a58d5734ab900af4a43c2018b533723145ed4f9c8272e3890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078370"
---
# <a name="tb_addstring-message"></a>Mensagem \_ ADDSTRING de TB

Adiciona uma nova cadeia de caracteres ao pool de cadeias de caracteres da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lidar com a instância do módulo com um arquivo executável que contém o recurso de cadeia de caracteres. Se *lParam, em vez* disso, aponta para uma matriz de caracteres com uma ou mais cadeias de caracteres, desmarque esse parâmetro como **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de recurso para o recurso de cadeia de caracteres ou um ponteiro para uma matriz TCHAR. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice da primeira nova cadeia de caracteres, se bem-sucedida, ou -1 caso contrário.

## <a name="remarks"></a>Comentários

Se *wParam* for **NULL,** *lParam* aponta para uma matriz de caracteres com uma ou mais cadeias de caracteres terminadas em nulo. A última cadeia de caracteres na matriz deve ser encerrada com dois caracteres nulos.

Se *wParam* for o HINSTANCE do aplicativo ou de outro módulo que contenha um recurso de cadeia de caracteres, *lParam* será o identificador de recurso da cadeia de caracteres. Cada item na cadeia de caracteres deve começar com um caractere separador arbitrário e a cadeia de caracteres deve terminar com dois desses caracteres. Por exemplo, o texto de três botões pode aparecer na tabela de cadeia de caracteres como "/New/Open/Save//". A mensagem retorna o índice de "Novo" no pool de cadeias de caracteres da barra de ferramentas e os outros itens estão em posições consecutivas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ ADDSTRINGW** (Unicode) e **TB \_ ADDSTRINGA** (ANSI)<br/>                 |



 

 





