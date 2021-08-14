---
title: Backup e restauração do Windows 7 preteridos
description: Backup e restauração do Windows 7 preteridos
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5975483797423515a4c04a35f8766de241553cb98a386bd53adcc7970977f7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211225"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Backup e restauração do Windows 7 preteridos

## <a name="platform"></a>Plataforma

**clientes** – Windows 8 


## <a name="description"></a>Descrição

Embora não haja nenhuma alteração comportamental para backup e restauração, essa função está sendo preterida e não será atualizada. Ele raramente era usado e sua funcionalidade foi substituída pelo novo recurso de histórico de arquivos. ele será fornecido em Windows 8 e entusiastas que fizeram a atualização do Windows 7 para Windows 8 ou dependem do backup e restauração ou do backup de imagem de disco ainda poderão usá-lo. No entanto, todos os pontos de acesso para backup e restauração, com exceção do painel de controle, foram removidos. o miniaplicativo do painel de controle usado pelo Backup e restauração foi renomeado para a recuperação de arquivo do Windows 7.

Os OEMs que estavam definindo a chave do registro para desabilitar a notificação de backup em suas imagens não precisarão mais fazer isso.

Não recomendamos o uso de ambos os recursos ao mesmo tempo. O histórico de arquivos verifica se o agendamento de backup existe e se está ativo e se encontra um, ele não permitirá que os usuários o ativem. nesse caso, os usuários que desejarem usar o histórico de arquivos precisarão excluir o agendamento de Backup do Windows.

## <a name="manifestation"></a>Manifestação

os fluxos de trabalho podem ser interrompidos e a documentação que se refere ao método anterior para acessar o recurso de Backup do Windows e restauração precisará ser atualizada para refletir essas alterações.

## <a name="mitigation"></a>Atenuação

Os aplicativos que podem disparar backup e restauração devem ser regravados para verificar se o histórico de arquivos está ativado e permitir que os usuários escolham seu método preferido.

 

 




