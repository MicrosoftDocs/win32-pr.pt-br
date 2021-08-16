---
description: Se essa política de sistema por computador for definida como 1, os patches não poderão ser removidos do computador por um usuário ou um administrador.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5531d5afd7fa98883a3e07dc7c47db625db9051fa223ea7cd6f70e4ceb5aee03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378564"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

Se essa política de sistema por [computador](system-policy.md) for definida como 1, os patches não poderão ser removidos do computador por um usuário ou um administrador. O Windows instalador de dados ainda pode remover um patch que não é mais aplicável a um produto. Se essa política não estiver definida, um usuário poderá remover um patch do computador somente se o usuário tiver privilégios para remover o patch. Isso pode depender se o usuário é um administrador, se as configurações de política [DisableMsi](disablemsi.md) e [AlwaysInstallElevated](alwaysinstallelevated.md) estão definidas e se o patch foi instalado em um contexto gerenciado por usuário, não gerenciado por usuário ou por computador.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



