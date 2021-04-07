---
description: Quando o instalador processa o script de instalação, ele gera um script de reversão simultaneamente.
ms.assetid: 5b9bfc5a-6a78-4b0e-aed8-f25aba089af1
title: Reverter ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c4ad91f8f94145399d51ed2ef53999ab0a91d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827600"
---
# <a name="rollback-custom-actions"></a>Reverter ações personalizadas

Quando o instalador processa o script de instalação, ele gera um script de reversão simultaneamente. Além do script de reversão, o instalador salva uma cópia de cada arquivo que ele exclui durante a instalação. Esses arquivos são mantidos em um diretório de sistema oculto. Quando a instalação for concluída, o script de reversão e os arquivos salvos serão excluídos. Se uma instalação não for bem-sucedida, o instalador tentará reverter as alterações feitas durante a instalação e restaurar o estado original do computador.

Embora as ações personalizadas que agendam operações do sistema inserindo linhas na tabela de banco de dados são revertidas por uma reversão da instalação, as ações personalizadas que alteram o sistema diretamente ou que emitem comandos para outros serviços do sistema não podem ser sempre revertidas por uma reversão. Uma ação personalizada de reversão é uma ação que o instalador executa somente durante uma reversão de instalação, e sua finalidade é reverter uma ação personalizada que tenha feito alterações no sistema.

Uma ação personalizada de reversão é um tipo de [ação personalizada de execução adiada](deferred-execution-custom-actions.md), porque sua execução é adiada quando é invocada durante a sequência de instalação. Ele difere de uma ação personalizada regular adiada, pois ela só é executada durante uma reversão. Uma ação personalizada de reversão sempre deve preceder a ação personalizada adiada que é revertida na sequência de ação. Uma ação personalizada de reversão também deve lidar com o caso em que a ação personalizada adiada é interrompida no meio da execução. Por exemplo, se o usuário fosse pressionar o botão Cancelar enquanto a ação personalizada estava em execução.

Observe que a reversão de ações personalizadas não pode ser executada de modo assíncrono. Consulte [ações personalizadas síncronas e assíncronas](synchronous-and-asynchronous-custom-actions.md).

O complemento a uma ação personalizada de reversão é uma [ação personalizada de confirmação](commit-custom-actions.md). O instalador executa uma ação personalizada de confirmação durante a sequência de instalação, copia a ação personalizada no script de reversão, mas não executa a ação durante a reversão.

Observe que uma ação personalizada de reversão pode não ser capaz de remover todas as alterações feitas por ações personalizadas de confirmação. Embora o instalador grave as ações de reversão e confirmação personalizada no script de reversão, as ações personalizadas de confirmação são executadas somente depois que o instalador tiver processado com êxito o script de instalação. As ações personalizadas de confirmação são as primeiras ações a serem executadas no script de reversão. Se uma ação personalizada de confirmação falhar, o instalador iniciará a reversão, mas só poderá reverter as operações já gravadas no script de reversão. Isso significa que, dependendo da ação personalizada de confirmação, uma reversão pode não ser capaz de desfazer as alterações feitas pela ação. Você pode ignorar as falhas em confirmar ações personalizadas, criando a ação personalizada para ignorar códigos de retorno.

Quando o instalador executa uma ação de reversão personalizada, o único parâmetro de modo que ele definirá é MSIRUNMODE \_ Rollback. Consulte [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para obter uma descrição dos parâmetros do modo de execução.

Uma ação personalizada de reversão pode ser especificada adicionando um sinalizador de opção ao campo tipo da [tabela CustomAction](customaction-table.md). Consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md) para o sinalizador de opção que designa uma ação personalizada de reversão.

As ações personalizadas de reversão e confirmação não são executadas quando a reversão está desabilitada. Se um autor de pacote exigir esses tipos de ações personalizadas para a instalação adequada, eles deverão usar a propriedade [**RollbackDisabled**](rollbackdisabled.md) em uma condição que impeça a instalação de continuar quando a reversão estiver desabilitada. Para obter informações sobre como desabilitar a reversão, consulte [Rollback Installation (Windows Installer)](rollback-installation.md).

 

 



