---
title: Apêndice F Valores do identificador de objeto para OBJID_QUERYCLASSNAMEIDX
description: Quando o OLEACC envia uma mensagem WM GETOBJECT com o parâmetro lParam definido como \_ OBJIDQUERYCLASSNAMEIDX, muitos controles COMUNS ou DE USUÁRIO padrão (COMCTL) retornam um dos valores a seguir.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22368f15fa40e30f909f9ad838cb478ed1e9a9c9ff25929f63bb91ec99e99b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134029"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Apêndice F: Valores do identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX

Quando o OLEACC envia uma mensagem [**WM \_ GETOBJECT**](wm-getobject.md) com o parâmetro *lParam* definido como OBJIDQUERYCLASSNAMEIDX, muitos controles COMUNS ou DE USUÁRIO padrão (COMCTL) retornam um dos valores a seguir.



| USUÁRIO ou controle comum | Valor retornado |
|------------------------|--------------|
| Listbox                | 65536+0      |
| Botão                 | 65536+2      |
| Estático                 | 65536+3      |
| Editar                   | 65536+4      |
| Combobox               | 65536+5      |
| Scrollbar              | 65536+10     |
| Status                 | 65536+11     |
| Barra de ferramentas                | 65536+12     |
| Progresso               | 65536+13     |
| Animar                | 65536+14     |
| Tab                    | 65536+15     |
| Tecla de acesso                 | 65536+16     |
| Cabeçalho                 | 65536+17     |
| Trackbar               | 65536+18     |
| Listview               | 65536+19     |
| Updown                 | 65536+22     |
| Dicas               | 65536+24     |
| Treeview               | 65536+25     |
| Richedit               | 65536+28     |



 

Somente USER e Windows comCTL (controles comuns) retornarão um dos valores da tabela. Se uma janela retornar 0 em resposta a essa mensagem, a janela poderá ser uma das seguintes:

-   Um controle personalizado
-   Um controle diferente de um dos controles na tabela anterior
-   Uma versão antiga de um controle do sistema que não reconhece a [**mensagem WM \_ GETOBJECT**](wm-getobject.md)

Se uma janela retornar 0, os clientes talvez precisem usar [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) ou [**GetClassName.**](/windows/win32/api/winuser/nf-winuser-getclassname) Você pode usar essas funções para determinar o tipo de controle com base no nome da classe.

Em geral, os clientes podem usar as informações fornecidas pelo OLEACC.

 

 