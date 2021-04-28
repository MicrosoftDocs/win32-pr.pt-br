---
description: Somente 64 bits
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: Somente 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088804"
---
# <a name="64-bit-only"></a>Somente 64 bits

## <a name="affected-platforms"></a>Plataformas afetadas

**Servidores** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -alta  






## <a name="description"></a>Descrição

O Windows Server 2008 R2 é fornecido com um SKU de 64 bits apenas; nenhuma SKU de 32 bits está disponível para a versão do servidor do sistema operacional. No entanto, um SKU de 32 bits continua disponível para o cliente do Windows 7.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

Isso afetará três áreas:

-   drivers de 32 bits
-   plug-ins de 32 bits
-   executáveis de 16 bits

## <a name="solution-for-32-bit-drivers"></a>Solução para drivers de 32 bits

Recompile drivers de 32 bits como drivers de 64 bits assinados.

## <a name="solution-for-32-bit-plug-ins"></a>Solução para plug-ins de 32 bits

O WoW64, um emulador x86, permite que aplicativos baseados em Windows de 32 bits sejam executados diretamente em janelas de 64 bits. O WoW64 agora é um recurso opcional que você deve instalar se for necessário executar o código de 32 bits.

O sistema isola os aplicativos de 32 bits de aplicativos de 64 bits, o que inclui a prevenção de colisões de arquivo e registro. Há suporte para aplicativos de console, GUI e serviço. O sistema fornece interoperabilidade entre o limite de 32/64 para cenários como recortar e colar e COM. No entanto, os processos de 32 bits não podem carregar DLLs de 64 bits e os processos de 64 bits não podem carregar DLLs de 32 bits. Normalmente vemos isso nos plug-ins do Shell escritos para o Windows Explorer.

Um aplicativo de 32 bits pode detectar se ele está em execução no WOW64 chamando a função IsWow64Process. O aplicativo pode obter informações adicionais sobre o processador usando a função GetNativeSystemInfo

Observe que o Windows de 64 bits não oferece suporte à execução de aplicativos baseados no Windows de 16 bits. O principal motivo é que os identificadores têm 32 bits significativos no Windows de 64 bits. Portanto, os identificadores não podem ser truncados e passados para aplicativos de 16 bits sem perda de dados. As tentativas de iniciar aplicativos de 16 bits falham com o seguinte erro: erro de \_ \_ formato exe inválido \_ .

## <a name="solution-for-16-bit-executables"></a>Solução para executáveis de 16 bits

o Windows de 64 bits reconhece um número limitado de programas de instalação de 16 bits específicos e substitui uma versão de 32 bits portada. A lista de substituições é armazenada no registro na seguinte chave: HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64 há suporte interno para vários mecanismos de instalação, incluindo instaladores do InstallShield 5. x. Observe que o Windows Installer de 64 bits pode instalar diretamente aplicativos baseados em MSI de 32 bits em janelas de 64 bits.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Executando aplicativos de 32 bits](/windows/desktop/WinProg64/running-32-bit-applications)
-   [Desempenho e consumo de memória](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [Detalhes da implementação do WOW64](/windows/desktop/WinProg64/wow64-implementation-details)
-   [Redirecionador de registro](/windows/desktop/WinProg64/registry-redirector)
-   [Redirecionador do sistema de arquivos](/windows/desktop/WinProg64/file-system-redirector)
-   [Gerenciamento de memória](/windows/desktop/WinProg64/memory-management)
-   [Afinidade do Processador](/windows/desktop/WinProg64/processor-affinity)
-   [Comunicação entre processos](/windows/desktop/WinProg64/interprocess-communication)
-   [Instalação de aplicativos em sistemas de 64 bits](/windows/desktop/WinProg64/application-installation)
-   [Depurando WOW64](/windows/desktop/WinProg64/debugging-wow64)
-   [**Função IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [**Função GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
