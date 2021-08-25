---
title: Mensagem de ACM_OPEN (commctrl. h)
description: Abre um clipe AVI e exibe seu primeiro quadro em um controle de animação. Você pode enviar essa mensagem explicitamente ou usar a \_ macro animado abrir ou animar \_ OpenEx. É recomendável usar a versão Unicode desta mensagem, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- controles de Windows de mensagem de ACM_OPEN
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5af2bd996af159217c92d78102a97e5c530d34cf445d5ad34186cecb93ab85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922166"
---
# <a name="acm_open-message"></a>\_Mensagem aberta do ACM

Abre um clipe AVI e exibe seu primeiro quadro em um controle de animação. Você pode enviar essa mensagem explicitamente ou usar a macro [**animado \_ abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ou [**animar \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) . É recomendável usar a versão Unicode desta mensagem, ACM \_ OPENW.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

[Versão 4,71](common-control-versions.md) e posterior. Um identificador de instância para o módulo do qual o recurso deve ser carregado. Defina esse valor como **NULL** para que o controle use o valor HINSTANCE usado para criar a janela. Observe que, se a janela for criada por uma DLL, o valor padrão para *wParam* será o valor HINSTANCE da dll, não do aplicativo que chama a dll.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um buffer que contém o caminho do arquivo AVI ou o nome de um recurso AVI. Como alternativa, esse parâmetro pode consistir no identificador de recurso AVI em [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e zero no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Para criar esse valor, use a macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) . O controle carrega o recurso AVI do módulo especificado pelo identificador de instância passado para a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , a macro de criação de [**animação \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) ou a função de criação da caixa de diálogo que criou o controle. Na [versão 4,71](common-control-versions.md) e posteriores, o recurso é carregado do módulo especificado por *wParam*. Um recurso AVI deve ter o tipo "AVI". Se esse parâmetro for **nulo**, o sistema fechará o arquivo AVI que foi aberto anteriormente para o controle de animação especificado, se houver.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

O arquivo AVI ou o recurso especificado por *lpszName* não deve conter áudio.

É recomendável usar a versão Unicode desta mensagem, ACM \_ OPENW.

Você só pode abrir clipes AVI silenciosos. Abrir \_ e [**animar \_ abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) falhará se *lParam* especificar um clipe AVI que contenha som.

Você pode usar a [**animação \_ fechar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) para fechar um arquivo AVI ou um recurso AVI que foi aberto anteriormente para o controle de animação especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **ACM \_ OPENW** (Unicode) e **ACM \_ opena** (ANSI)<br/>                         |



 

