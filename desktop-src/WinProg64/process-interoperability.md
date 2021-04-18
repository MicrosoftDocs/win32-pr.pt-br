---
title: Interoperabilidade de processo
description: Você pode executar aplicativos baseados em Win32 no Windows de 64 bits usando uma camada de emulação. O Windows 10 no ARM inclui uma camada de emulação x86-on-ARM64. Para obter mais informações, consulte Executando aplicativos de 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- Programação de processo de interoperabilidade do Windows de 64 bits
- Programação de interoperabilidade do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760570"
---
# <a name="process-interoperability"></a>Interoperabilidade de processo

Você pode executar aplicativos baseados em Win32 no Windows de 64 bits usando uma camada de emulação. O Windows 10 no ARM inclui uma camada de emulação x86-on-ARM64. Para obter mais informações, consulte [executando aplicativos de 32 bits](running-32-bit-applications.md).

No Windows de 64 bits, um processo de 64 bits não pode carregar uma DLL (biblioteca de vínculo dinâmico) de 32 bits. Além disso, um processo de 32 bits não pode carregar uma DLL de bit 64. No entanto, o Windows de 64 bits dá suporte a RPC (chamadas de procedimento remoto) entre processos de 64 bits e de 32 bits (no mesmo computador e entre computadores). No Windows de 64 bits, um servidor COM de 32 bits de bit insuficiente pode se comunicar com um cliente de 64 bits e um servidor COM de 64-bit fora do processo pode se comunicar com um cliente de 32 bits. Portanto, se você tiver uma DLL de 32 bits que não reconheça o COM, poderá encapsulá-la em um servidor COM fora do processo e usar COM para realizar marshaling de chamadas para e de um processo de 64 bits.

Atualmente, os servidores em processo são registrados usando a entrada de registro **InprocServer** . No Windows de 64 bits, os servidores de 64 e 32 bits em processo devem usar a entrada **InprocServer32** .

Para identificadores de porta, que por sua natureza são locais para o computador e nunca seriam usados em um limite de 32 bits a 64 bits, use o **tipo \_ PTR de identificador** em vez do tipo PTR **\_ PTR** ou **DWORD \_** . Isso inclui portar interfaces RPC passando tais identificadores como valores **DWORD** . O identificador de 64 **bits \_ PTR** é de 64 bits na conexão (não truncado) e, portanto, não precisa de mapeamento. (O identificador de 32 **bits \_ PTR** é de 32 bits na conexão.)

Para obter mais informações, consulte [Criando interfaces compatíveis com 64 bits](designing-64-bit-compatible-interfaces.md).

 

 




