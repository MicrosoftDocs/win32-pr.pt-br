---
description: A ação InstallFinalize executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a execução das ações InstallExecute ou InstallExecuteAgain.
ms.assetid: ed0e3c4f-d1ee-43b7-84a2-f4afe3ec28c6
title: Ação InstallFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db8bd3ac9473fab868e5f7d83e760b39ca4dd6136faec987b5a7d2a3777bdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787036"
---
# <a name="installfinalize-action"></a>Ação InstallFinalize

A ação InstallFinalize executa um script que contém todas as operações na sequência de ação desde o início da instalação ou a execução das ações [InstallExecute](installexecute-action.md) ou [InstallExecuteAgain](installexecuteagain-action.md) . Esta ação marca o final de uma transação que começa com a ação [InstallInitialize](installinitialize-action.md) .

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação [InstallInitialize](installinitialize-action.md) deve vir antes da ação InstallFinalize.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

Se for detectado que o produto está marcado para remoção completa, as operações serão adicionadas automaticamente ao script para remover a **adição/remoção de programas** nas informações do **painel de controle** do produto, para cancelar o registro e cancelar a publicação do produto e remover o banco de dados local armazenado em cache de% Windows%, se existir.

As alterações do sistema feitas antes da ação não podem ser restauradas depois que a ação InstallFinalize é executada. A ação InstallFinalize atualiza o sistema com todas as operações determinadas para esse ponto e, em seguida, encerra a transação.

 

 



