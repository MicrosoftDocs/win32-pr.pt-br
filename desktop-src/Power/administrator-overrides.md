---
description: Substituições do administrador
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Substituições do administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af73f6d6fe3fe7d4edb8272c4d39c385a84973e4a3263c448505f5235adec855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033016"
---
# <a name="administrator-overrides"></a>Substituições do administrador

Windows tem uma única ACL (lista de controle de acesso) padrão em todos os objetos de política de energia. A ACL concede permissões de leitura, gravação e alteração aos membros do grupo de usuários autenticados. Todos os outros usuários recebem permissão somente leitura. Aplicativos que chamam funções de política de energia podem determinar se um usuário tem permissões para uma configuração de energia especificada usando a função [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .

As configurações de energia podem ser substituídas por meio de Política de Grupo. As substituições podem ser definidas por meio da política de grupo de domínio ou da política de grupo local. [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) relatará se uma configuração de energia especificada tiver uma substituição de política de grupo.

A ferramenta de linha de comando **PowerCfg.exe** exibe uma mensagem de erro quando um comando não pode ser concluído porque o usuário não tinha permissões para alterar a configuração de energia ou porque a configuração de energia tem uma substituição de política de grupo.

O aplicativo opções de energia no painel de controle não fornece suporte para configurar permissões de acesso à política de energia. A alteração de permissões deve ser feita via **PowerCfg.exe**.

 

 



