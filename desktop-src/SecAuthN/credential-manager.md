---
description: Um Gerenciador de credenciais é semelhante a um provedor de rede no que fornece pontos de entrada chamados pelo roteador de vários provedores (MPR). Na verdade, alguns provedores de rede também são gerenciadores de credenciais.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Gerenciador de Credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20165a5e6145de0a2c042c38923c41d793bd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011248"
---
# <a name="credential-manager"></a>Gerenciador de Credenciais

Um Gerenciador de credenciais é semelhante a um provedor de rede no que fornece pontos de entrada chamados pelo [*roteador de vários provedores*](/windows/desktop/SecGloss/m-gly) (MPR). Na verdade, alguns provedores de rede também são gerenciadores de credenciais.

Se você implementar as funções de gerenciamento de credenciais na mesma DLL que as funções de provedor de rede depende dos requisitos do seu aplicativo. Os gerenciadores de credenciais recebem notificações quando as informações de autenticação são alteradas. Por exemplo, os gerenciadores de credenciais são notificados quando um usuário faz logon ou uma conta de senha é alterada. Quando um processo de logon, como o [*Winlogon*](/windows/desktop/SecGloss/w-gly), está no processo de fazer logon ou alterar a senha de uma conta, ele chama a função de WNet (rede do Windows) de MPR apropriada. Em seguida, o MPR chama o ponto de entrada apropriado para cada Gerenciador de credenciais. Essas funções de gerenciamento de credenciais sempre serão chamadas no contexto do sistema, LocalSystem, em vez do contexto do usuário. Para obter mais informações sobre as funções do WNet, consulte [sistema de rede do Windows](/windows/desktop/WNet/windows-networking-wnet-). Para obter mais informações sobre a interface que os gerenciadores de credenciais devem implementar, consulte [**API de gerenciamento de credenciais**](credential-management-api.md).

 

 
