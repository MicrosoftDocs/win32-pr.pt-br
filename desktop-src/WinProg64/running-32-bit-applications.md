---
title: Executando aplicativos de 32 bits
description: Execute aplicativos baseados no Windows de 32 bits diretamente no Windows de 64 bits com o emulador x86 do WOW64. Além disso, saiba mais sobre o diretor do registro, o redirecionador de sistema de arquivos, a instalação de aplicativos em sistemas de 64 bits e a depuração de WOW64.
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- Programação WOW64 de 64 bits do Windows
- Programação WOW64 de 64 bits do Windows, sobre
- aplicativos de 32 bits em programação de 64 bits Windows 64-bit Windows Programming
- Guia de programação do Windows de 64 bits programação de Windows de 64 bits, WOW64 consulte WOW64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39872be28da0853f0cff62a9a0ab82065105c687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917357"
---
# <a name="running-32-bit-applications"></a>Executando aplicativos de 32 bits

O WOW64 é o emulador x86 que permite que aplicativos baseados no Windows de 32 bits sejam executados diretamente em janelas de 64 bits. Isso permite que os aplicativos do Windows de 32 bits (x86) sejam executados diretamente em Windows de 64 bits (x64), bem como para aplicativos do Windows de 32 bits (x86) e de 32 bits (ARM) para serem executados perfeitamente em janelas de 64 bits (ARM64). O WOW64 é fornecido com o sistema operacional e não precisa estar explicitamente habilitado. Para obter mais informações, consulte [detalhes de implementação do WOW64](wow64-implementation-details.md).

O sistema isola os aplicativos de 32 bits de aplicativos de 64 bits, o que inclui a prevenção de colisões de arquivo e registro. Há suporte para aplicativos de console, GUI e serviço. O sistema fornece interoperabilidade entre o limite de 32/64 para cenários como recortar e colar e COM. No entanto, os processos de 32 bits não podem carregar DLLs de 64 bits para execução, e processos de 64 bits não podem carregar DLLs de 32 bits para execução. Essa restrição não se aplica a DLLs carregadas como arquivos de dados ou arquivos de recurso de imagem; para obter mais informações, consulte [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).

Um aplicativo de 32 bits pode detectar se ele está em execução no WOW64 chamando a função [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) (use [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) se estiver direcionando para o Windows 10). O aplicativo pode obter informações adicionais sobre o processador usando a função [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

Observe que o Windows de 64 bits não oferece suporte à execução de aplicativos baseados no Windows de 16 bits. O principal motivo é que os identificadores têm 32 bits significativos no Windows de 64 bits. Portanto, os identificadores não podem ser truncados e passados para aplicativos de 16 bits sem perda de dados. As tentativas de iniciar aplicativos de 16 bits falham com o seguinte erro: **erro de \_ \_ \_ formato exe inválido**.

## <a name="in-this-section"></a>Nesta seção

-   [Desempenho e consumo de memória no WOW64](performance-and-memory-consumption.md)
-   [Detalhes da implementação do WOW64](wow64-implementation-details.md)
-   [Redirecionador de registro](registry-redirector.md)
-   [Redirecionador do sistema de arquivos](file-system-redirector.md)
-   [Gerenciamento de memória](memory-management.md)
-   [Afinidade do Processador](processor-affinity.md)
-   [Comunicação entre processos](interprocess-communication.md)
-   [Instalação de aplicativo](application-installation.md)
-   [Depurando WOW64](debugging-wow64.md)

 

 