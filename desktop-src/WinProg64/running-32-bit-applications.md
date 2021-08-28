---
title: Executando aplicativos de 32 bits
description: execute aplicativos baseados em Windows de 32 bits diretamente em Windows de 64 bits com o emulador do WOW64 x86. Além disso, saiba mais sobre o diretor do registro, o redirecionador de sistema de arquivos, a instalação de aplicativos em sistemas de 64 bits e a depuração de WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- programação de Windows de 64 bits WOW64
- programação de Windows de 64 bits de WOW64, sobre
- aplicativos de 32 bits em programação de 64 bits Windows de Windows de 64 bits
- guia de programação de Windows de 64 bits 64-Windows programação de bits, wow64 consulte wow64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1da192f4109afe09133f036d5fff88e772bbcc2c7d20ceb456e3233ab2b60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132819"
---
# <a name="running-32-bit-applications"></a>Executando aplicativos de 32 bits

o WOW64 é o emulador x86 que permite a execução direta de aplicativos baseados em Windows de 32 bits em Windows de 64 bits. isso permite que os aplicativos de 32 bits (x86) Windows sejam executados diretamente no Windows de 64 bits (x64), bem como para aplicativos de Windows de 32 bits (x86) e de 32 bits (ARM) para serem executados perfeitamente em Windows de 64 bits (ARM64). O WOW64 é fornecido com o sistema operacional e não precisa estar explicitamente habilitado. Para obter mais informações, consulte [detalhes de implementação do WOW64](wow64-implementation-details.md).

O sistema isola os aplicativos de 32 bits de aplicativos de 64 bits, o que inclui a prevenção de colisões de arquivo e registro. Há suporte para aplicativos de console, GUI e serviço. O sistema fornece interoperabilidade entre o limite de 32/64 para cenários como recortar e colar e COM. No entanto, os processos de 32 bits não podem carregar DLLs de 64 bits para execução, e processos de 64 bits não podem carregar DLLs de 32 bits para execução. Essa restrição não se aplica a DLLs carregadas como arquivos de dados ou arquivos de recurso de imagem; para obter mais informações, consulte [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Um aplicativo de 32 bits pode detectar se ele está em execução sob o WOW64 chamando a função [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) (use [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) se estiver direcionando Windows 10). O aplicativo pode obter informações adicionais sobre o processador usando a função [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

observe que o Windows de 64 bits não oferece suporte à execução de aplicativos baseados em Windows de 16 bits. O principal motivo é que os identificadores têm 32 bits significativos em Windows de 64 bits. Portanto, os identificadores não podem ser truncados e passados para aplicativos de 16 bits sem perda de dados. As tentativas de iniciar aplicativos de 16 bits falham com o seguinte erro: **erro de \_ \_ \_ formato exe inválido**.

## <a name="in-this-section"></a>Nesta seção

-   [Desempenho e consumo de memória no WOW64](performance-and-memory-consumption.md)
-   [Detalhes da implementação do WOW64](wow64-implementation-details.md)
-   [Redirecionador de registro](registry-redirector.md)
-   [Redirecionador do sistema de arquivos](file-system-redirector.md)
-   [Gerenciamento de memória](memory-management.md)
-   [Afinidade do Processador](processor-affinity.md)
-   [Comunicação entre processos](interprocess-communication.md)
-   [Instalação do aplicativo](application-installation.md)
-   [Depurando WOW64](debugging-wow64.md)

 

 