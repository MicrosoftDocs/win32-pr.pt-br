---
description: Use as constantes a seguir para identificar a sessão do agente do NT kernel.
ms.assetid: f64f05c1-b904-4847-8502-4abb9cf4d37f
title: Constantes do NT kernel logger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13767400ff851e358f6665c88e16767cc378a4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968185"
---
# <a name="nt-kernel-logger-constants"></a><span data-ttu-id="b673b-103">Constantes do NT kernel logger</span><span class="sxs-lookup"><span data-stu-id="b673b-103">NT Kernel Logger Constants</span></span>

<span data-ttu-id="b673b-104">Use as constantes a seguir para identificar a sessão do agente do NT kernel.</span><span class="sxs-lookup"><span data-stu-id="b673b-104">Use the following constants to identify the NT Kernel Logger session.</span></span>



| <span data-ttu-id="b673b-105">Constante</span><span class="sxs-lookup"><span data-stu-id="b673b-105">Constant</span></span>               | <span data-ttu-id="b673b-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b673b-106">Description</span></span>                                                      |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="b673b-107">SystemTraceControlGuid</span><span class="sxs-lookup"><span data-stu-id="b673b-107">SystemTraceControlGuid</span></span> | <span data-ttu-id="b673b-108">O GUID de controle da sessão de rastreamento de eventos do agente de log do NT kernel.</span><span class="sxs-lookup"><span data-stu-id="b673b-108">The control GUID for the NT Kernel Logger event tracing session.</span></span> |
| <span data-ttu-id="b673b-109">nome do agente de log do KERNEL \_ \_</span><span class="sxs-lookup"><span data-stu-id="b673b-109">KERNEL\_LOGGER\_NAME</span></span>   | <span data-ttu-id="b673b-110">O nome da sessão de rastreamento de eventos do agente de log do NT kernel.</span><span class="sxs-lookup"><span data-stu-id="b673b-110">The name of the NT Kernel Logger event tracing session.</span></span>          |



 

<span data-ttu-id="b673b-111">A sessão do NT kernel logger é a única sessão que pode aceitar eventos de provedores de eventos de kernel.</span><span class="sxs-lookup"><span data-stu-id="b673b-111">The NT Kernel Logger session is the only session that can accept events from kernel event providers.</span></span> <span data-ttu-id="b673b-112">A sessão do NT kernel Logger não aceita eventos de outros provedores.</span><span class="sxs-lookup"><span data-stu-id="b673b-112">The NT Kernel Logger session does not accept events from other providers.</span></span> <span data-ttu-id="b673b-113">Se você quiser capturar eventos e eventos de kernel de outros provedores, deverá usar duas sessões separadas e o consumidor precisaria mesclar os eventos dos arquivos de log para fornecer resultados de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="b673b-113">If you want to capture kernel events and events from other providers, you must use two separate sessions and the consumer would need to merge the events from the log files to provide end-to-end results.</span></span>

<span data-ttu-id="b673b-114">O ETW usa a \_ macro definir GUID para definir GUIDs.</span><span class="sxs-lookup"><span data-stu-id="b673b-114">ETW uses the DEFINE\_GUID macro to define GUIDs.</span></span> <span data-ttu-id="b673b-115">Para usar o **SystemTraceControlGuid** em seu código, você deve incluir \# definir Initguid antes de incluir Evntrace. h.</span><span class="sxs-lookup"><span data-stu-id="b673b-115">To use **SystemTraceControlGuid** in your code, you must include \#define INITGUID before including Evntrace.h.</span></span> <span data-ttu-id="b673b-116">O compilador então ativará o GUID de definição \_ em um GUID constante.</span><span class="sxs-lookup"><span data-stu-id="b673b-116">The compiler will then turn the DEFINE\_GUID into a constant GUID.</span></span>

<span data-ttu-id="b673b-117">Os valores a seguir definem os GUIDs de classe possíveis para eventos de kernel que uma sessão do agente de log do NT pode rastrear.</span><span class="sxs-lookup"><span data-stu-id="b673b-117">The following values define the possible class GUIDs for kernel events that an NT Kernel Logger session can trace.</span></span> <span data-ttu-id="b673b-118">Você pode passar os GUIDs de classe para a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) para configurar o processamento especial para cada classe de evento.</span><span class="sxs-lookup"><span data-stu-id="b673b-118">You can pass the class GUIDs to the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function to set up special processing for each event class.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b673b-119">Classe</span><span class="sxs-lookup"><span data-stu-id="b673b-119">Class</span></span></th>
<th><span data-ttu-id="b673b-120">GUID</span><span class="sxs-lookup"><span data-stu-id="b673b-120">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b673b-121"><a href="alpc.md"><strong>ALPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-121"><a href="alpc.md"><strong>ALPC</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 45d8cccd-539f-4b72-a8b7-5c683142609a */
    ALPCGuid,
    0x45d8cccd,
    0x539f,
    0x4b72,
    0xa8, 0xb7, 0x5c, 0x68, 0x31, 0x42, 0x60, 0x9a
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b673b-122"><a href="diskio.md"><strong>DiskIo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-122"><a href="diskio.md"><strong>DiskIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c */
    DiskIoGuid,
    0x3d6fa8d4,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b673b-123"><a href="hwconfig.md"><strong>HWConfig</strong></a> e <a href="systemconfig.md"> <strong>SystemConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-123"><a href="hwconfig.md"><strong>HWConfig</strong></a> and <a href="systemconfig.md"><strong>SystemConfig</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 01853a65-418f-4f36-aefc-dc0f1d2fd235 */
    EventTraceConfigGuid,
    0x01853a65,
    0x418f,
    0x4f36,
    0xae, 0xfc, 0xdc, 0x0f, 0x1d, 0x2f, 0xd2, 0x35
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b673b-124"><a href="fileio.md"><strong>FileIo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-124"><a href="fileio.md"><strong>FileIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 90cbdc39-4a3e-11d1-84f4-0000f80464e3 */
    FileIoGuid,
    0x90cbdc39,
    0x4a3e,
    0x11d1,
    0x84, 0xf4, 0x00, 0x00, 0xf8, 0x04, 0x64, 0xe3
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b673b-125"><a href="image.md"><strong>Imagem</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-125"><a href="image.md"><strong>Image</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 2cb15d1d-5fc1-11d2-abe1-00a0c911f518 */
    ImageLoadGuid,
    0x2cb15d1d,
    0x5fc1,
    0x11d2,
    0xab, 0xe1, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x18
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b673b-126"><a href="pagefault-v2.md"><strong>PageFault_V2</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-126"><a href="pagefault-v2.md"><strong>PageFault_V2</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c */
    PageFaultGuid,
    0x3d6fa8d3,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b673b-127"><a href="perfinfo.md"><strong>PerfInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-127"><a href="perfinfo.md"><strong>PerfInfo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* ce1dbfb4-137e-4da6-87b0-3f59aa102cbc */
    PerfInfoGuid,
    0xce1dbfb4,
    0x137e,
    0x4da6,
    0x87, 0xb0, 0x3f, 0x59, 0xaa, 0x10, 0x2c, 0xbc
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b673b-128"><a href="process.md"><strong>Processar</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-128"><a href="process.md"><strong>Process</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c */
    ProcessGuid,
    0x3d6fa8d0,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b673b-129"><a href="registry.md"><strong>Registro</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-129"><a href="registry.md"><strong>Registry</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* AE53722E-C863-11d2-8659-00C04FA321A1 */
    RegistryGuid, 
    0xae53722e,
    0xc863,
    0x11d2,
    0x86, 0x59, 0x0, 0xc0, 0x4f, 0xa3, 0x21, 0xa1
);</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b673b-130"><a href="splitio.md"><strong>SplitIo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-130"><a href="splitio.md"><strong>SplitIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* d837ca92-12b9-44a5-ad6a-3a65b3578aa8 */
    SplitIoGuid, 
    0xd837ca92,
    0x12b9,
    0x44a5,
    0xad, 0x6a, 0x3a, 0x65, 0xb3, 0x57, 0x8a, 0xa8
);</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b673b-131"><a href="tcpip.md"><strong>IP</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-131"><a href="tcpip.md"><strong>TcpIp</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 9a280ac0-c8e0-11d1-84e2-00c04fb998a2 */
    TcpIpGuid,
    0x9a280ac0,
    0xc8e0,
    0x11d1,
    0x84, 0xe2, 0x00, 0xc0, 0x4f, 0xb9, 0x98, 0xa2
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b673b-132"><a href="thread.md"><strong>Processo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-132"><a href="thread.md"><strong>Thread</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c */
    ThreadGuid,
    0x3d6fa8d1,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b673b-133"><a href="udpip.md"><strong>UdpIp</strong></a></span><span class="sxs-lookup"><span data-stu-id="b673b-133"><a href="udpip.md"><strong>UdpIp</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* bf3a50c5-a9c9-4988-a005-2df0b7c80f80 */
    UdpIpGuid,
    0xbf3a50c5,
    0xa9c9,
    0x4988,
    0xa0, 0x05, 0x2d, 0xf0, 0xb7, 0xc8, 0x0f, 0x80
  );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b673b-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b673b-134">Remarks</span></span>

<span data-ttu-id="b673b-135">Para usar os GUIDs, copie as definições de GUID que você deseja usar para o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="b673b-135">To use the GUIDs, copy the GUID definitions that you want to use to your source code.</span></span> <span data-ttu-id="b673b-136">Você deve incluir \# definir Initguid antes das definições que você inclui em seu código-fonte, portanto, o compilador ativará o GUID de definição \_ em um GUID constante.</span><span class="sxs-lookup"><span data-stu-id="b673b-136">You must include \#define INITGUID before the definitions you include in your source code, so the compiler will turn the DEFINE\_GUID into a constant GUID.</span></span> <span data-ttu-id="b673b-137">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="b673b-137">For example,</span></span>

``` syntax
#define INITGUID

DEFINE_GUID ( /* 3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c */
    ThreadGuid,
    0x3d6fa8d1,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );

DEFINE_GUID ( /* 3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c */
    ProcessGuid,
    0x3d6fa8d0,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );
```

<span data-ttu-id="b673b-138">Como alternativa, você pode definir o GUID de constante para as definições de GUID por conta própria.</span><span class="sxs-lookup"><span data-stu-id="b673b-138">As an alternative, you can define the constant GUID for the GUID definitions yourself.</span></span> <span data-ttu-id="b673b-139">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="b673b-139">For example,</span></span>

``` syntax
static const GUID ThreadGuid = 
{ 0x3d6fa8d0, 0xfe05, 0x11d0, { 0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c } };
```

 

 
