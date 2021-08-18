---
title: Interoperabilidade de processo
description: você pode executar aplicativos baseados em Win32 em Windows de 64 bits usando uma camada de emulação. Windows 10 no ARM inclui uma camada de emulação x86-on-ARM64. Para obter mais informações, consulte Executando aplicativos de 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- programação de Windows bits de interoperabilidade de processo 64-bit
- programação de Windows bits de interoperabilidade 64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74e75af4299e9c249ea46b8eac2cdd47de10eb3f832aa88d6b313d20304afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561512"
---
# <a name="process-interoperability"></a>Interoperabilidade de processo

você pode executar aplicativos baseados em Win32 em Windows de 64 bits usando uma camada de emulação. Windows 10 no ARM inclui uma camada de emulação x86-on-ARM64. Para obter mais informações, consulte [executando aplicativos de 32 bits](running-32-bit-applications.md).

no Windows de 64 bits, um processo de 64 bits não pode carregar uma DLL (biblioteca de vínculo dinâmico) de 32 bits. Além disso, um processo de 32 bits não pode carregar uma DLL de bit 64. no entanto, o Windows de 64 bits dá suporte a chamadas de procedimento remoto (RPC) entre processos de 64 bits e de 32 bits (no mesmo computador e entre computadores). no Windows de 64 bits, um servidor com de 32 bits sem processo pode se comunicar com um cliente de 64 bits e um servidor com de 64-bit de não processo pode se comunicar com um cliente de 32 bits. Portanto, se você tiver uma DLL de 32 bits que não reconheça o COM, poderá encapsulá-la em um servidor COM fora do processo e usar COM para realizar marshaling de chamadas para e de um processo de 64 bits.

Atualmente, os servidores em processo são registrados usando a entrada de registro **InprocServer** . no Windows de 64 bits, os servidores de 64 e 32 bits em processo devem usar a entrada **InprocServer32** .

Para identificadores de porta, que por sua natureza são locais para o computador e nunca seriam usados em um limite de 32 bits a 64 bits, use o **tipo \_ PTR de identificador** em vez do tipo PTR **\_ PTR** ou **DWORD \_** . Isso inclui portar interfaces RPC passando tais identificadores como valores **DWORD** . O identificador de 64 **bits \_ PTR** é de 64 bits na conexão (não truncado) e, portanto, não precisa de mapeamento. (O identificador de 32 **bits \_ PTR** é de 32 bits na conexão.)

Para obter mais informações, consulte [Criando interfaces compatíveis com 64 bits](designing-64-bit-compatible-interfaces.md).

 

 




