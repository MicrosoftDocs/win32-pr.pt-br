---
title: Classes e servidores
description: Classes e servidores
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366764"
---
# <a name="classes-and-servers"></a>Classes e servidores

COM usa **a \_ \_ raiz de classes hKey** para configurações de todo o computador, mas também permite a configuração por usuário de CLSIDs para maior segurança e flexibilidade. O COM primeiro consulta o **HKEY \_ Current \_ user \\ software \\ classes** antes de examinar a **\_ \_ raiz de classes hKey**. O COM mantém informações em todo o computador relacionadas a CLSIDs em classe **HKEY \_ \_ raiz \\ CLSID** e mantém as informações de classes por usuário em **HKEY \_ Current \_ user \\ software \\ classes \\ CLSID**.

Os servidores COM oferecem suporte ao auto-registro. Para um servidor em processo, isso significa que a DLL deve exportar as seguintes funções:

-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

Você deve exportar explicitamente essas funções usando um arquivo de definição de módulo, opções de vinculador ou diretivas de compilador. O repositório de classe usa essas funções para configurar o registro local depois de baixar o arquivo para o computador cliente. Além do armazenamento de classe, essas funções também são usadas por outros ambientes para instalar servidores em computadores host.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 