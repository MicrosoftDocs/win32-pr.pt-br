---
description: Essa é uma política de sistema por máquina que pode ser usada quando o administrador desejar apenas aplicativos por máquina instalados.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 171c003dbe739c890bf15e5c372e40840fee0aabc9159a837c0b5572a8741b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378509"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

Essa é uma [política de sistema](system-policy.md) por máquina que pode ser usada quando o administrador desejar apenas aplicativos por máquina instalados.

Se essa política não estiver definida, o instalador pesquisará o registro em busca de aplicativos na seguinte ordem: aplicativos gerenciados registrados como aplicativos por usuário e não gerenciados registrados como por usuário e, por fim, aplicativos registrados como por máquina.

Se essa política for definida como 1, o instalador ignorará todos os aplicativos registrados como por usuário e somente procurará por aplicativos registrados como por computador. chamadas para a interface de programação de aplicativo Windows Installer ou o sistema ignoram aplicativos por usuário. Uma tentativa de executar uma instalação no [contexto de instalação](installation-context.md) por usuário faz com que o instalador exiba uma mensagem de erro e pare a instalação. nesse caso, o Windows Installer também impede instalações por usuário de um servidor de terminal.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer** de políticas de Software de computador LOCAL

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



