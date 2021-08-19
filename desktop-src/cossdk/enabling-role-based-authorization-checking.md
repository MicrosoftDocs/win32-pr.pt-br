---
description: Para usar a segurança baseada em função em seu aplicativo COM+, você deve primeiro habilitar a verificação de autorização baseada em função para o aplicativo.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Habilitando Role-Based verificação de autorização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd46a0b09b981a3dd7731f5839458550379dad5619f22d1caaaddb24e87deaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813854"
---
# <a name="enabling-role-based-authorization-checking"></a>Habilitando Role-Based verificação de autorização

Para usar a segurança baseada em função em seu aplicativo COM+, você deve primeiro habilitar a verificação de autorização baseada em função para o aplicativo. Isso garante que os usuários que estão acessando o aplicativo sejam verificados quanto à função à que pertencem antes que eles sejam autorizados a fazer qualquer coisa no aplicativo. Se a verificação de autorização baseada em função não estiver habilitada, a segurança baseada em função para o aplicativo não será usada.

**Para habilitar a verificação de autorização baseada em função**

1.  Clique com o botão direito do mouse no aplicativo COM+ para o qual você está habilitando a verificação de autorização baseada em função e clique em **Propriedades**.

2.  Na caixa de diálogo propriedades do aplicativo, clique na **guia** Segurança.

3.  Em **Autorização**, marque a **caixa de seleção Impor verificações** de acesso para este aplicativo; limpar a caixa de seleção significa que a segurança baseada em função não é usada para o aplicativo.

4.  Clique em **OK**.

A configuração de autorização selecionada entra em vigor na próxima vez que o aplicativo for iniciado.

 

 



