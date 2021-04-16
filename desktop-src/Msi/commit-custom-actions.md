---
description: As ações personalizadas de confirmação são executadas após a conclusão bem-sucedida do script de instalação.
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: Confirmar ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174af16a84f71ff90a1fc35c76054ee503449b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758313"
---
# <a name="commit-custom-actions"></a>Confirmar ações personalizadas

As ações personalizadas de confirmação são executadas após a conclusão bem-sucedida do script de instalação. Se a [ação InstallFinalize](installfinalize-action.md) for bem-sucedida, o instalador executará qualquer ação personalizada de confirmação existente. O único parâmetro de modo que o instalador define nesse caso é MSIRUNMODE \_ Commit. Consulte [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para obter uma descrição dos parâmetros do modo de execução.

Uma ação personalizada Commit pode ser especificada adicionando um sinalizador Option ao campo Type da [tabela CustomAction](customaction-table.md). Consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md) para o sinalizador de opção que designa uma ação personalizada de confirmação.

Uma ação personalizada de confirmação é o complemento a uma [ação personalizada de reversão](rollback-custom-actions.md) e pode ser usada com ações de reversão personalizadas para reverter ações personalizadas que fazem alterações diretamente no sistema.

Observe que uma ação personalizada de reversão pode não ser capaz de remover todas as alterações feitas por ações personalizadas de confirmação. Embora o instalador grave as ações de reversão e confirmação personalizada no script de reversão, as ações personalizadas de confirmação são executadas somente depois que o instalador tiver processado com êxito o script de instalação. As ações personalizadas de confirmação são as primeiras ações a serem executadas no script de reversão. Se uma ação personalizada de confirmação falhar, o instalador iniciará a reversão, mas só poderá reverter as operações já gravadas no script de reversão. Isso significa que, dependendo da ação personalizada de confirmação, uma reversão pode não ser capaz de desfazer as alterações feitas pela ação. Você pode ignorar as falhas em confirmar ações personalizadas, criando a ação personalizada para ignorar códigos de retorno.

As ações personalizadas de reversão e confirmação não são executadas quando a reversão está desabilitada. Se um autor de pacote exigir esses tipos de ações personalizadas para a instalação adequada, eles deverão usar a propriedade [**RollbackDisabled**](rollbackdisabled.md) em uma condição que impeça a instalação de continuar quando a reversão estiver desabilitada.

 

 



