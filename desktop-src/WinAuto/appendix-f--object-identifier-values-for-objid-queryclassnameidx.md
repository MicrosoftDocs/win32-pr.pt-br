---
title: Apêndice F valores de identificador de objeto para OBJID_QUERYCLASSNAMEIDX
description: Quando OLEACC envia uma \_ mensagem do WM GetObject com o parâmetro lParam definido como OBJIDQUERYCLASSNAMEIDX, muitos usuários padrão ou controles comuns (COMCTL) retornam um dos valores a seguir.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810731"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a>Apêndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX

Quando OLEACC envia uma mensagem do [**WM \_ GetObject**](wm-getobject.md) com o parâmetro *lParam* definido como OBJIDQUERYCLASSNAMEIDX, muitos usuários padrão ou controles comuns (COMCTL) retornam um dos valores a seguir.



| USUÁRIO ou controle comum | Retornar valor |
|------------------------|--------------|
| Caixas                | 65536 + 0      |
| Botão                 | 65536 + 2      |
| Estático                 | 65536 + 3      |
| Editar                   | 65536 + 4      |
| Combobox               | 65536 + 5      |
| Rolagem              | 65536 + 10     |
| Status                 | 65536 + 11     |
| Barra de ferramentas                | 65536 + 12     |
| Progresso               | 65536 + 13     |
| Animar                | 65536 + 14     |
| Tab                    | 65536 + 15     |
| Tecla de acesso                 | 65536 + 16     |
| parâmetro                 | 65536 + 17     |
| TrackBar               | 65536 + 18     |
| Fotos               | 65536 + 19     |
| Updown                 | 65536 + 22     |
| Dicas               | 65536 + 24     |
| TreeView               | 65536 + 25     |
| RichEdit               | 65536 + 28     |



 

Somente o usuário e os COMCTL (controles comuns do Windows) retornarão um dos valores da tabela. Se uma janela retornar 0 em resposta a essa mensagem, a janela poderá ser uma das seguintes:

-   Um controle personalizado
-   Um controle diferente de um dos controles na tabela anterior
-   Uma versão antiga de um controle do sistema que não reconhece a mensagem do [**WM \_ GetObject**](wm-getobject.md)

Se uma janela retornar 0, os clientes talvez precisem usar [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) ou [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname). Você pode usar essas funções para determinar o tipo de controle com base no nome da classe.

Em geral, os clientes podem usar as informações fornecidas pelo OLEACC.

 

 