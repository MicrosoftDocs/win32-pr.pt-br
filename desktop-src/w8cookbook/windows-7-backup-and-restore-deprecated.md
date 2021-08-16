---
title: Windows 7 Backup e Restauração preterido
description: Windows 7 Backup e Restauração preterido
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
# <a name="windows-7-backup-and-restore-deprecated"></a>Windows 7 Backup e Restauração preterido

## <a name="platform"></a>Plataforma

**Clientes** – Windows 8 


## <a name="description"></a>Descrição

Embora não haja nenhuma alteração comportamental para Backup e Restauração, essa função está sendo preterida e não será atualizada. Ele raramente foi usado e sua funcionalidade foi substituída pelo novo Histórico de Arquivos recurso. Ele será Windows 8 e os entusiados que atualizaram do Windows 7 para o Windows 8 ou dependem do backup e restauração ou backup de imagem de disco ainda poderão usá-lo. No entanto, todos os pontos de acesso para Backup e Restauração, com exceção do Painel de Controle, foram removidos. O Painel de Controle applet usado pelo Backup e Restauração foi renomeado para Windows Recuperação de Arquivos 7.

Os OEMs que estavam definindo a chave do Registro para desabilitar a notificação de backup em suas imagens não precisarão mais fazer isso.

Não recomendamos o uso de ambos os recursos ao mesmo tempo. Histórico de Arquivos verifica se o agendamento de backup existe e se está ativo e, se encontrar um, ele não permitirá que os usuários o a liguem. Nesse caso, os usuários que quiserem usar Histórico de Arquivos terão que excluir o Backup do Windows agendamento.

## <a name="manifestation"></a>Manifestação

Os fluxos de trabalho podem ser interrompidos e a documentação que se refere ao método anterior para acessar o Backup do Windows e o recurso De restauração precisarão ser atualizados para refletir essas alterações.

## <a name="mitigation"></a>Atenuação

Os aplicativos que podem disparar Backup e Restauração devem ser reescritos para verificar se Histórico de Arquivos está ativado e permitir que os usuários escolham seu método preferencial.

 

 




