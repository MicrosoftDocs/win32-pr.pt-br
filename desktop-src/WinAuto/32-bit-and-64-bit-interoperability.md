---
title: interoperabilidade de 32 bits e 64 bits
description: Os aplicativos de tecnologia assistencial precisam se comunicar entre limites de processo para obter informações de interface do usuário de Microsoft Acessibilidade Ativa Servers e provedores de automação da interface do usuário da Microsoft.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c056c9fe2792734e9369fa311e69528ce226f7edf15b82440b63c12c52de66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327985"
---
# <a name="32-bit-and-64-bit-interoperability"></a>interoperabilidade de 32 bits e 64 bits

Os aplicativos de tecnologia assistencial precisam se comunicar entre limites de processo para obter informações de interface do usuário de Microsoft Acessibilidade Ativa Servers e provedores de automação da interface do usuário da Microsoft. este tópico descreve os principais problemas de comunicação entre processos que você precisa ter em mente ao desenvolver Windows aplicativos de acessibilidade.

quando os aplicativos usam a API de automação Windows, os componentes de tempo de execução de automação da interface do usuário e da Microsoft Acessibilidade Ativa lidam automaticamente com todos os problemas e as complexidades envolvidas na execução de IPC (comunicações entre processos), incluindo os problemas de interoperabilidade envolvidos quando um processo é de 32 bits e o outro é de 64 bits. a Microsoft reconhece que há ocasiões em que um aplicativo de tecnologia assistencial pode precisar usar alguma forma de IPC em vez da API de automação de Windows para se comunicar com um Microsoft Acessibilidade Ativa server ou um provedor de automação de interface do usuário. nessas ocasiões, a Microsoft recomenda que você use as mensagens DCOM ou Windows (aquelas com valores menores do que o do **WM \_ USER**) para se comunicar com outros processos. assim como a API de automação Windows, as mensagens DCOM e Windows lidam automaticamente com todos os problemas de IPC, incluindo a interoperabilidade de 32 bits para 64 bits.

quando as mensagens API de automação Windows, DCOM e Windows não forem uma opção, tenha em mente os seguintes problemas ao implementar o método IPC escolhido:

-   Memória compartilhada — ao usar a memória compartilhada, lembre-se de que uma estrutura em um processo de 32 bits pode ter um tamanho e um layout diferentes da mesma estrutura em um processo de 64 bits. Isso é especialmente verdadeiro para estruturas que contêm ponteiros ou identificadores.
-   truncamento de ponteiro — embora um aplicativo de 32 bits possa usar o tipo de dados **LONGLONG** para armazenar um valor de 64 bits, há instâncias em que não existe nenhum elemento API de Windows que permita que o aplicativo de 32 bits receba um valor de 64 de um processo de 64 bits ou envie um valor de 64 bits para um processo de 64 bits. Por exemplo, as funções [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) e [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) truncam todos os valores de ponteiro, deixando o aplicativo de 32 bits com um valor inútil.
-   Identificadores — como os identificadores Kernel32 e user32 são apenas de 32 bits significativos em processos de 32 bits e de 64 bits, eles podem ser transferidos entre processos sem problemas. no entanto, alguns itens que Windows define como identificadores são, na verdade, apenas ponteiros encapsulados (por exemplo, **HTREEITEM**). Esses "identificadores" serão truncados se forem passados de um processo de 64 bits para um processo de 32 bits.
-   [WinEvent](winevents-infrastructure.md) Funções de gancho — para registrar uma função de gancho no contexto com um processo de servidor de 32 bits, a função Hook deve residir em uma DLL de 32 bits. Da mesma forma, para registrar uma função de gancho no contexto com um processo de servidor de 64 bits, a função Hook deve residir em uma DLL de 64 bits. Se um aplicativo de tecnologia assistencial tentar registrar uma função de gancho no contexto com um servidor que tenha uma profundidade de bits diferente, os eventos ainda serão entregues à função de gancho, mas serão entregues fora de contexto. Para obter mais informações, consulte [funções de gancho WinEvents e in-context e out-of-Context](in-context-and-out-of-context-hook-functions.md).

Para obter mais informações sobre a interoperabilidade de 32 bits e 64 bits, consulte [interoperabilidade de processo](/windows/desktop/WinProg64/process-interoperability).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Visão geral da API de automação](windows-automation-api-overview.md)
</dt> </dl>

 

 