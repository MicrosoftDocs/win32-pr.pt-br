---
title: Mensagem de CQPM_HELP (Cmnquery. h)
description: Enviado para a função de retorno de chamada CQPageProc de uma página de extensão de formulário de consulta para permitir que a extensão de página exiba a ajuda contextual para a página.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- Mensagem de CQPM_HELP Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085256"
---
# <a name="cqpm_help-message"></a>Mensagem de ajuda do CQPM \_

A mensagem de **\_ ajuda do CQPM** é enviada para a função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de uma página de extensão do formulário de consulta para permitir que a extensão de página exiba a ajuda contextual para a página. Se possível, a extensão de página de consulta deve exibir a ajuda contextual em resposta a esse evento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contém dados adicionais sobre o item de menu, controle, caixa de diálogo ou janela para o qual a ajuda contextual é solicitada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa mensagem é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

