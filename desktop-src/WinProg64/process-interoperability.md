---
title: Interoperabilidade de processo
description: Você pode executar aplicativos baseados em Win32 em um Windows de 64 bits usando uma camada de emulação. Windows 10 no ARM inclui uma camada de emulação x86-on-ARM64. Para obter mais informações, consulte Executando aplicativos de 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- interoperabilidade de processo de programação Windows 64 bits
- programação de 64 bits Windows interoperabilidade
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

Você pode executar aplicativos baseados em Win32 em um Windows de 64 bits usando uma camada de emulação. Windows 10 no ARM inclui uma camada de emulação x86-on-ARM64. Para obter mais informações, consulte [Executando aplicativos de 32 bits.](running-32-bit-applications.md)

Em uma Windows de 64 bits, um processo de 64 bits não pode carregar uma DLL (biblioteca de vínculo dinâmico) de 32 bits. Além disso, um processo de 32 bits não pode carregar uma DLL de 64 bits. No entanto, o Windows de 64 bits dá suporte a RPC (chamadas de procedimento remoto) entre processos de 64 e 32 bits (no mesmo computador e em computadores). No Windows de 64 bits, um servidor COM de 32 bits fora do processo pode se comunicar com um cliente de 64 bits e um servidor COM de 64 bits fora do processo pode se comunicar com um cliente de 32 bits. Portanto, se você tiver uma DLL de 32 bits que não esteja ciente de COM, poderá wrap-lo em um servidor COM fora do processo e usar COM para fazer marshal de chamadas para e de um processo de 64 bits.

Atualmente, os servidores em processo são registrados usando a entrada do Registro **InprocServer.** Em servidores em processo de 64 Windows, servidores em processo de 64 e 32 bits devem usar a **entrada InprocServer32.**

Para identificador de porta, que, por sua natureza, são locais para o computador e nunca seriam usados entre o limite de 32 bits a 64 bits, use o tipo **\_ HANDLE PTR** em vez do tipo **\_ PTR INT** ou **DWORD \_ PTR.** Isso inclui a portação de interfaces RPC passando alças como **valores DWORD.** O **\_ PTR handle** de 64 bits é de 64 bits na transmissão (não truncado) e, portanto, não precisa de mapeamento. (O **\_ PTR** de HANDLE de 32 bits é de 32 bits na transmissão.)

Para obter mais informações, consulte [Projetando interfaces compatíveis com 64 bits.](designing-64-bit-compatible-interfaces.md)

 

 




