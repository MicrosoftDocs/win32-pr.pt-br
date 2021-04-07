---
description: Se essa política do sistema por máquina for definida como 1, os patches não poderão ser removidos do computador por um usuário ou um administrador.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827351"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

Se essa [política do sistema](system-policy.md) por máquina for definida como 1, os patches não poderão ser removidos do computador por um usuário ou um administrador. O Windows Installer ainda pode remover um patch que não é mais aplicável a um produto. Se essa política não estiver definida, um usuário poderá remover um patch do computador somente se o usuário tiver concedido privilégios para remover o patch. Isso pode depender se o usuário é um administrador, se as configurações de política [DisableMsi](disablemsi.md) e [AlwaysInstallElevated](alwaysinstallelevated.md) estão definidas e se o patch foi instalado em um contexto gerenciado por usuário, não gerenciado por usuário ou por computador.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



