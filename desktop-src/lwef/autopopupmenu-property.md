---
title: Propriedade AutoPopupMenu
description: Propriedade AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292572"
---
# <a name="autopopupmenu-property"></a>Propriedade AutoPopupMenu

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define se clicar com o botão direito do mouse no caractere ou no ícone da barra de tarefas exibirá automaticamente o menu pop-up do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do. ***Caracteres * * * * ("*** characterid * * *"). AutoPopupMenu* *  \[  =  *booliano*\]



| Parte      | Descrição                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o servidor exibe automaticamente o menu pop-up do caractere no clique com o botão direito do mouse. **True** (padrão) exibe o menu ao clicar com o botão direito do mouse. <br/> **Falso** Não exibe o menu ao clicar com o botão direito do mouse.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao definir essa propriedade como **false**, você pode criar seu próprio comportamento de manipulação de menus. Para exibir o menu depois de definir essa propriedade como **false**, use o método [**ShowPopupMenu**](showpopupmenu-method.md) .

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**Método ShowPopupMenu**](showpopupmenu-method.md)


 

 





