---
description: Para usar a segurança baseada em função em seu aplicativo COM+, primeiro você deve habilitar a verificação de autorização baseada em função para o aplicativo.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Habilitando a verificação de autorização de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010230"
---
# <a name="enabling-role-based-authorization-checking"></a>Habilitando a verificação de autorização de Role-Based

Para usar a segurança baseada em função em seu aplicativo COM+, primeiro você deve habilitar a verificação de autorização baseada em função para o aplicativo. Isso garante que os usuários que estão acessando o aplicativo sejam verificados para a função à qual pertencem antes que estejam autorizados a fazer qualquer coisa no aplicativo. Se a verificação de autorização baseada em função não estiver habilitada, a segurança baseada em função para o aplicativo não será usada.

**Para habilitar a verificação de autorização baseada em função**

1.  Clique com o botão direito do mouse no aplicativo COM+ para o qual você está habilitando a verificação de autorização baseada em função e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .

3.  Em **autorização**, marque a caixa de seleção **impor verificações de acesso para este aplicativo** ; desmarcar a caixa de seleção significa que a segurança baseada em função não é usada para o aplicativo.

4.  Clique em **OK**.

A configuração de autorização selecionada entrará em vigor na próxima vez em que o aplicativo for iniciado.

 

 



