---
description: Se essa política de sistema por computador não estiver definida, somente os administradores poderão corrigir os produtos existentes que foram instalados usando privilégios elevados.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c827b23f8beecf02d3312358d7ece6b835619111428349850f4e597ce379cd53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145899"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

Se essa política de [sistema](system-policy.md) por computador não estiver definida, somente os administradores poderão corrigir os produtos existentes que foram instalados usando privilégios elevados. Se AllowLockdownPatch estiver definido como "1", os usuários não administrativos poderão, em alguns casos, aplicar patches aos produtos durante a execução de uma instalação usando privilégios elevados. Com o conjunto de políticas, o patch pode instalar atualizações [secundárias](minor-upgrades.md) durante a execução de uma instalação usando privilégios elevados, o patch não pode instalar [atualizações principais.](major-upgrades.md) Definir essa política também permite que usuários não administrativos executem programas em privilégios localSystem durante uma instalação com privilégios elevados.

A configuração padrão é recomendada para garantir um ambiente seguro.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Qualquer usuário pode aplicar um patch durante uma instalação nãolevada. Definir essa política [](system-policy.md) de sistema por computador como "1" oferece aos usuários não administrativas a flexibilidade adicional de aplicar patches a qualquer produto durante uma instalação elevada. Se essa política não estiver definida, os usuários não administrativas não poderão aplicar um patch a aplicativos atribuídos ou publicados.

Definir essa política também permite que usuários não administrativos executem programas arbitrários em privilégios localSystem se eles têm um pacote de patch do instalador do Windows que instala ou inicia esses programas.

 

 



