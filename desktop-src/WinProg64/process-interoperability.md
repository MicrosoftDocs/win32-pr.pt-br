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
# <a name="process-interoperability"></a><span data-ttu-id="7f603-107">Interoperabilidade de processo</span><span class="sxs-lookup"><span data-stu-id="7f603-107">Process Interoperability</span></span>

<span data-ttu-id="7f603-108">Você pode executar aplicativos baseados em Win32 no Windows de 64 bits usando uma camada de emulação.</span><span class="sxs-lookup"><span data-stu-id="7f603-108">You can run Win32-based applications on 64-bit Windows using an emulation layer.</span></span> <span data-ttu-id="7f603-109">O Windows 10 no ARM inclui uma camada de emulação x86-on-ARM64.</span><span class="sxs-lookup"><span data-stu-id="7f603-109">Windows 10 on ARM includes an x86-on-ARM64 emulation layer.</span></span> <span data-ttu-id="7f603-110">Para obter mais informações, consulte [executando aplicativos de 32 bits](running-32-bit-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7f603-110">For more information, see [Running 32-bit Applications](running-32-bit-applications.md).</span></span>

<span data-ttu-id="7f603-111">No Windows de 64 bits, um processo de 64 bits não pode carregar uma DLL (biblioteca de vínculo dinâmico) de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7f603-111">On 64-bit Windows, a 64-bit process cannot load a 32-bit dynamic-link library (DLL).</span></span> <span data-ttu-id="7f603-112">Além disso, um processo de 32 bits não pode carregar uma DLL de bit 64.</span><span class="sxs-lookup"><span data-stu-id="7f603-112">Additionally, a 32-bit process cannot load a 64-bit DLL.</span></span> <span data-ttu-id="7f603-113">No entanto, o Windows de 64 bits dá suporte a RPC (chamadas de procedimento remoto) entre processos de 64 bits e de 32 bits (no mesmo computador e entre computadores).</span><span class="sxs-lookup"><span data-stu-id="7f603-113">However, 64-bit Windows supports remote procedure calls (RPC) between 64-bit and 32-bit processes (both on the same computer and across computers).</span></span> <span data-ttu-id="7f603-114">No Windows de 64 bits, um servidor COM de 32 bits de bit insuficiente pode se comunicar com um cliente de 64 bits e um servidor COM de 64-bit fora do processo pode se comunicar com um cliente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7f603-114">On 64-bit Windows, an out-of-process 32-bit COM server can communicate with a 64-bit client, and an out-of-process 64-bit COM server can communicate with a 32-bit client.</span></span> <span data-ttu-id="7f603-115">Portanto, se você tiver uma DLL de 32 bits que não reconheça o COM, poderá encapsulá-la em um servidor COM fora do processo e usar COM para realizar marshaling de chamadas para e de um processo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7f603-115">Therefore, if you have a 32-bit DLL that is not COM-aware, you can wrap it in an out-of-process COM server and use COM to marshal calls to and from a 64-bit process.</span></span>

<span data-ttu-id="7f603-116">Atualmente, os servidores em processo são registrados usando a entrada de registro **InprocServer** .</span><span class="sxs-lookup"><span data-stu-id="7f603-116">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="7f603-117">No Windows de 64 bits, os servidores de 64 e 32 bits em processo devem usar a entrada **InprocServer32** .</span><span class="sxs-lookup"><span data-stu-id="7f603-117">On 64-bit Windows, 64- and 32-bit in-process servers should use the **InprocServer32** entry.</span></span>

<span data-ttu-id="7f603-118">Para identificadores de porta, que por sua natureza são locais para o computador e nunca seriam usados em um limite de 32 bits a 64 bits, use o **tipo \_ PTR de identificador** em vez do tipo PTR **\_ PTR** ou **DWORD \_** .</span><span class="sxs-lookup"><span data-stu-id="7f603-118">To port handles, which by their nature are local to the computer and would never be used across the 32-bit to 64-bit boundary, use the **HANDLE\_PTR** type instead of the **INT\_PTR** or **DWORD\_PTR** type.</span></span> <span data-ttu-id="7f603-119">Isso inclui portar interfaces RPC passando tais identificadores como valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7f603-119">This includes porting RPC interfaces passing such handles as **DWORD** values.</span></span> <span data-ttu-id="7f603-120">O identificador de 64 **bits \_ PTR** é de 64 bits na conexão (não truncado) e, portanto, não precisa de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="7f603-120">The 64-bit **HANDLE\_PTR** is 64 bits on the wire (not truncated) and thus does not need mapping.</span></span> <span data-ttu-id="7f603-121">(O identificador de 32 **bits \_ PTR** é de 32 bits na conexão.)</span><span class="sxs-lookup"><span data-stu-id="7f603-121">(The 32-bit **HANDLE\_PTR** is 32 bits on the wire.)</span></span>

<span data-ttu-id="7f603-122">Para obter mais informações, consulte [Criando interfaces compatíveis com 64 bits](designing-64-bit-compatible-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7f603-122">For more information, see [Designing 64-bit-Compatible Interfaces](designing-64-bit-compatible-interfaces.md).</span></span>

 

 




