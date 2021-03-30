---
title: interoperabilidade de 32 bits e 64 bits
description: Os aplicativos de tecnologia assistencial precisam se comunicar entre limites de processo para obter informações de interface do usuário de Microsoft Acessibilidade Ativa Servers e provedores de automação da interface do usuário da Microsoft.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6897082db00e27d77d90e5fc72d5f229834ce760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641384"
---
# <a name="32-bit-and-64-bit-interoperability"></a>interoperabilidade de 32 bits e 64 bits

Os aplicativos de tecnologia assistencial precisam se comunicar entre limites de processo para obter informações de interface do usuário de Microsoft Acessibilidade Ativa Servers e provedores de automação da interface do usuário da Microsoft. Este tópico descreve os principais problemas de comunicação entre processos que você precisa ter em mente ao desenvolver aplicativos de acessibilidade do Windows.

Quando os aplicativos usam a API de automação do Windows, os componentes de tempo de execução do Microsoft Acessibilidade Ativa e da interface do usuário lidam automaticamente com todos os problemas e as complexidades envolvidas na execução de IPC (comunicações entre processos), incluindo os problemas de interoperabilidade envolvidos quando um processo é de 32 bits e o outro é de 64 bits. A Microsoft reconhece que há ocasiões em que um aplicativo de tecnologia assistencial pode precisar usar alguma forma de IPC em vez da API de automação do Windows para se comunicar com um Microsoft Acessibilidade Ativa Server ou um provedor de automação de interface do usuário. Nessas ocasiões, a Microsoft recomenda que você use mensagens DCOM ou do Windows (aquelas com valores menores do que o do **WM \_ User**) para se comunicar com outros processos. Assim como a API de automação do Windows, as mensagens DCOM e Windows lidam automaticamente com todos os problemas de IPC, incluindo a interoperabilidade de 32 bits a 64 bits.

Quando as mensagens API de automação do Windows, DCOM e Windows não são uma opção, tenha em mente os seguintes problemas ao implementar o método IPC escolhido:

-   Memória compartilhada — ao usar a memória compartilhada, lembre-se de que uma estrutura em um processo de 32 bits pode ter um tamanho e um layout diferentes da mesma estrutura em um processo de 64 bits. Isso é especialmente verdadeiro para estruturas que contêm ponteiros ou identificadores.
-   Truncamento de ponteiro — embora um aplicativo de 32 bits possa usar o tipo de dados **LONGLONG** para armazenar um valor de 64 bits, há instâncias em que não existe nenhum elemento da API do Windows que permitisse que o aplicativo de 32 bits receba um valor de 64 bits de um processo de 64 bits ou envie um valor de 64 bits para um processo de 64 bits. Por exemplo, as funções [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) e [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) truncam todos os valores de ponteiro, deixando o aplicativo de 32 bits com um valor inútil.
-   Identificadores — como os identificadores Kernel32 e user32 são apenas de 32 bits significativos em processos de 32 bits e de 64 bits, eles podem ser transferidos entre processos sem problemas. No entanto, alguns itens que o Windows define como identificador são, na verdade, apenas ponteiros encapsulados (por exemplo, **HTREEITEM**). Esses "identificadores" serão truncados se forem passados de um processo de 64 bits para um processo de 32 bits.
-   [WinEvent](winevents-infrastructure.md) Funções de gancho — para registrar uma função de gancho no contexto com um processo de servidor de 32 bits, a função Hook deve residir em uma DLL de 32 bits. Da mesma forma, para registrar uma função de gancho no contexto com um processo de servidor de 64 bits, a função Hook deve residir em uma DLL de 64 bits. Se um aplicativo de tecnologia assistencial tentar registrar uma função de gancho no contexto com um servidor que tenha uma profundidade de bits diferente, os eventos ainda serão entregues à função de gancho, mas serão entregues fora de contexto. Para obter mais informações, consulte [funções de gancho WinEvents e in-context e out-of-Context](in-context-and-out-of-context-hook-functions.md).

Para obter mais informações sobre a interoperabilidade de 32 bits e 64 bits, consulte [interoperabilidade de processo](/windows/desktop/WinProg64/process-interoperability).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da API de automação do Windows](windows-automation-api-overview.md)
</dt> </dl>

 

 