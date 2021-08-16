---
description: Se essa política de sistema por computador estiver definida como &\# 0034;1&0034;, o instalador impedirá que não administradores usem a Aplicação de Patch de UAC (Controle de Conta de Usuário) para qualquer aplicativo instalado no \# computador.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821eb480ac09a2fc0416d7b3a54c0df5699a7096b45e56a843afe691886296f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637773"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Se essa política de sistema por computador estiver definida como "1", o instalador impedirá que não administradores usem a Aplicação de Patch [UAC (Controle](user-account-control--uac--patching.md) de Conta de Usuário) para qualquer aplicativo instalado no computador. Quando a política do sistema por computador não está definida ou definida como 0, os não administradores podem aplicar patches de usuário com privilégios mínimos a aplicativos habilitados para a aplicação de patch de conta de usuário com privilégios mínimos.

Use a [**propriedade MSIDISABLELUAPATCHING**](msidisableluapatching.md) para evitar a aplicação de patch de privilégios mínimos de um aplicativo.

A política DisableLUAPatching está disponível a partir do Windows Installer versão 3.0.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



