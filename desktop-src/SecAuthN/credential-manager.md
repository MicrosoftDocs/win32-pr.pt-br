---
description: Um gerenciador de credenciais é semelhante a um provedor de rede, já que ele fornece pontos de entrada que são chamados pelo MPR (roteador de vários provedores). Na verdade, alguns provedores de rede também são gerenciadores de credenciais.
ms.assetid: a1105754-a57f-4a0d-9797-bec22b99900c
title: Gerenciador de Credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a33b1a47ff17123a1974823d7fee1421df7755850d46d2992fec51f62f5fac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008824"
---
# <a name="credential-manager"></a>Gerenciador de Credenciais

Um gerenciador de credenciais é semelhante a um provedor de rede, já que ele fornece pontos de entrada que são chamados pelo MPR [*(roteador de vários*](/windows/desktop/SecGloss/m-gly) provedores). Na verdade, alguns provedores de rede também são gerenciadores de credenciais.

Se você implementa as funções de gerenciamento de credenciais na mesma DLL que as funções do provedor de rede depende dos requisitos do seu aplicativo. Os gerenciadores de credenciais recebem notificações quando as informações de autenticação são mudadas. Por exemplo, os gerenciadores de credenciais são notificados quando um usuário faz login ou uma senha de conta é mudada. Quando um processo de logon, como [*o Winlogon,*](/windows/desktop/SecGloss/w-gly)está no processo de fazer logon ou alterar a senha de uma conta, ele chama a função de rede WNet (rede Windows MPR) apropriada. Em seguida, a MPR chama o ponto de entrada apropriado para cada gerenciador de credenciais. Essas funções de gerenciamento de credenciais sempre serão chamadas no contexto do sistema, LocalSystem, em vez do contexto do usuário. Para obter mais informações sobre funções WNet, consulte [Windows Rede.](/windows/desktop/WNet/windows-networking-wnet-) Para obter mais informações sobre a interface que os gerenciadores de credenciais devem implementar, consulte [**Credential API de Gerenciamento**](credential-management-api.md).

 

 
