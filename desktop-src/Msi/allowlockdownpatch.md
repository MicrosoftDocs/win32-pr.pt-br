---
description: Se essa política do sistema por máquina não estiver definida, somente os administradores poderão corrigir os produtos existentes que foram instalados usando privilégios elevados.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921521"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

Se essa [política do sistema](system-policy.md) por máquina não estiver definida, somente os administradores poderão corrigir os produtos existentes que foram instalados usando privilégios elevados. Se AllowLockdownPatch for definido como "1", os usuários não administrativos poderão, em alguns casos, aplicar patches aos produtos enquanto executam uma instalação usando privilégios elevados. Com a política definida, o patch pode instalar [pequenas atualizações](minor-upgrades.md) ao executar uma instalação usando privilégios elevados, o patch não pode instalar as [principais atualizações](major-upgrades.md). Definir essa política também permite que usuários não administrativos executem programas em privilégios LocalSystem durante uma instalação elevada.

A configuração padrão é recomendada para garantir um ambiente seguro.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Qualquer usuário pode aplicar um patch durante uma instalação não elevada. Definir essa [política de sistema](system-policy.md) por máquina como "1" fornece aos usuários não administrativos a flexibilidade adicional de aplicar patches a qualquer produto durante uma instalação elevada. Se essa política não estiver definida, os usuários não administrativos não poderão aplicar um patch a aplicativos atribuídos ou publicados.

Definir essa política também permite que usuários não administrativos executem programas arbitrários em privilégios LocalSystem se tiverem um pacote de patches Windows Installer que instala ou inicia esses programas.

 

 



