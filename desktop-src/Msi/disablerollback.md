---
description: Se essa política do sistema for definida como 1, o instalador não armazenará arquivos de retorção durante a instalação e desabilitará a reação da instalação.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da8380ce5dc7ea0b711d5766a554d6dce970bc81587a75164e61f3694c6a5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947310"
---
# <a name="disablerollback"></a>DisableRollback

Se essa [política do sistema](system-policy.md) for definida como 1, o instalador não armazenará arquivos de retorção durante a instalação e desabilitará a reação da instalação. Por padrão, a reação está habilitada. Os administradores são aconselhados a não usar essa política, a menos que seja absolutamente essencial. Para obter mais informações, consulte [Instalação de re rollback](rollback-installation.md).

## <a name="registry-key"></a>Chave do Registro

Para desabilitar a re reação para instalações por usuário, de definido **DisableRollback** como 1 na seguinte chave do Registro:

**HKEY \_ Atual \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

Para desabilitar a reação para instalações por computador, de acordo com **DisableRollback** como 1 na chave do Registro a seguir.

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



