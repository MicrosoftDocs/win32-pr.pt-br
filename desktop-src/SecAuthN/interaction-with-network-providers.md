---
description: Explica as interações entre o Winlogon e os provedores de rede.
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: Interação com provedores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829758"
---
# <a name="interaction-with-network-providers"></a>Interação com provedores de rede

Você pode configurar um sistema para dar suporte a zero ou mais provedores de rede. Cada um desses provedores de rede pode especificar que ele requer processamento de autenticação interativa especial. Esse recurso permite que as redes instaladas coletem informações de identificação e de autenticação específicas para cada rede, mas, ainda assim, permitem que elas as coletem durante o logon normal e sob a proteção segura do [*contexto*](../secgloss/c-gly.md) e da área de trabalho [*do Winlogon*](../secgloss/w-gly.md) .

O Winlogon chama provedores de rede em várias circunstâncias. Após um logon bem-sucedido, o Winlogon chama os provedores de rede para que eles possam coletar [*credenciais*](../secgloss/c-gly.md) e autenticar o usuário para sua rede. O Winlogon também chama provedores de rede quando os usuários alteram suas senhas. Isso permite que cada usuário mantenha uma única senha para uso em todas as redes.

A estrutura de [**\_ informações de \_ notificação \_ do WLX MPR**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) é usada para fornecer informações de identificação e autenticação nas funções de Gina relevantes. Essa estrutura inclui os membros a seguir.



| Membro             | DESCRIÇÃO                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszUserName**    | O nome da conta do usuário conectado.                                                                                                                                                      |
| **pszDomain**      | O nome de domínio do usuário conectado. Nem todos os modelos de autenticação têm um conceito de domínio (ou seu equivalente), portanto, esse membro pode ser **nulo**.                                              |
| **pszPassword**    | Quando o usuário forneceu uma senha de texto sem formatação durante a autenticação, fornecê-la aqui permite que outros provedores de rede usem a mesma senha (para obter logon único) sem avisar o usuário.    |
| **pszOldPassword** | Após uma alteração de senha, fornecendo a senha original aqui e a nova senha no membro **pszPassword** , permite que os provedores de rede atualizem suas senhas sem avisar o usuário. |



 

Uma [*Gina*](../secgloss/g-gly.md) não precisa fornecer essas informações aos provedores de rede. Se um ponteiro **NULL** for passado em vez de um ponteiro de estrutura válido, os provedores de rede solicitarão as informações ao usuário.

 

 
