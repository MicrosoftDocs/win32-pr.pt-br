---
title: Classes e servidores
description: Classes e servidores
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b87ce6b52e73f8ac4e465202b787a2c65dc563f3d7c0678ef82b91601351d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993796"
---
# <a name="classes-and-servers"></a>Classes e servidores

O COM **usa o \_ \_ HKEY CLASSES ROOT** para configurações de todo o computador, mas também permite a configuração por usuário de CLSIDS para maior segurança e flexibilidade. O COM primeiro consulta classes de software **do usuário atual HKEY \_ \_ \\ \\** antes de procurar em **HKEY \_ CLASSES \_ ROOT**. O COM mantém informações de todo o computador relacionadas a CLSIDs em **\_ \_ \\ CLSID** RAIZ de CLASSES HKEY e mantém informações de classe por usuário em **\_ \_ \\ \\ \\ CLSID** de classes de software do usuário atual HKEY .

Os servidores COM são suportados por auto-registro. Para um servidor em processo, isso significa que a DLL deve exportar as seguintes funções:

-   [**Dllregisterserver**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**Dllunregisterserver**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

Você deve exportar explicitamente essas funções usando um arquivo de definição de módulo, opções de vinculador ou diretivas do compilador. O armazenamento de classes usa essas funções para configurar o registro local depois de baixar o arquivo no computador cliente. Além do armazenamento de classes, essas funções também são usadas por outros ambientes para instalar servidores em computadores host.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 