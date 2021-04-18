---
description: Substituições do administrador
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Substituições do administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758927"
---
# <a name="administrator-overrides"></a>Substituições do administrador

O Windows tem uma única ACL (lista de controle de acesso) padrão em todos os objetos de política de energia. A ACL concede permissões de leitura, gravação e alteração aos membros do grupo de usuários autenticados. Todos os outros usuários recebem permissão somente leitura. Aplicativos que chamam funções de política de energia podem determinar se um usuário tem permissões para uma configuração de energia especificada usando a função [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .

As configurações de energia podem ser substituídas por meio de Política de Grupo. As substituições podem ser definidas por meio da política de grupo de domínio ou da política de grupo local. [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) relatará se uma configuração de energia especificada tiver uma substituição de política de grupo.

A ferramenta de linha de comando **PowerCfg.exe** exibe uma mensagem de erro quando um comando não pode ser concluído porque o usuário não tinha permissões para alterar a configuração de energia ou porque a configuração de energia tem uma substituição de política de grupo.

O aplicativo opções de energia no painel de controle não fornece suporte para configurar permissões de acesso à política de energia. A alteração de permissões deve ser feita via **PowerCfg.exe**.

 

 



