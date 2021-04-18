---
description: Se essa política do sistema por máquina estiver definida como &\# 0034; 1&\# 0034;, o instalador impedirá que não administradores usem a aplicação de patches do controle de conta de usuário (UAC) para qualquer aplicativo instalado no computador.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778724"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Se essa política do sistema por máquina for definida como "1", o instalador impedirá que não administradores usem a [aplicação de patch do controle de conta de usuário (UAC)](user-account-control--uac--patching.md) para qualquer aplicativo instalado no computador. Quando a política do sistema por máquina não é definida ou definida como 0, os não administradores podem aplicar patches de usuário com privilégios mínimos a aplicativos habilitados para patches de conta de usuário com privilégios mínimos.

Use a propriedade [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) para impedir a aplicação de patches com privilégios mínimos de um aplicativo.

A política DisableLUAPatching está disponível a partir do Windows Installer versão 3,0.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



