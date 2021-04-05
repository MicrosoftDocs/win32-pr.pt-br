---
description: Este tópico contém informações sobre APIs de nível baixo que são usadas pela infraestrutura de cliente do Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Suporte de cliente variado Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826080"
---
# <a name="miscellaneous-low-level-client-support"></a><span data-ttu-id="21bfb-103">Suporte de cliente variado Low-Level</span><span class="sxs-lookup"><span data-stu-id="21bfb-103">Miscellaneous Low-Level Client Support</span></span>

<span data-ttu-id="21bfb-104">Este tópico contém informações sobre APIs de nível baixo que são usadas pela infraestrutura de cliente do Windows.</span><span class="sxs-lookup"><span data-stu-id="21bfb-104">This topic contains information about low-level APIs that are used by the Windows client infrastructure.</span></span>

### <a name="functions"></a><span data-ttu-id="21bfb-105">Funções</span><span class="sxs-lookup"><span data-stu-id="21bfb-105">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21bfb-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="21bfb-106">Topic</span></span></th>
<th><span data-ttu-id="21bfb-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="21bfb-107">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21bfb-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-109">A função _lclose fecha o arquivo especificado para que ele não fique mais disponível para leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="21bfb-109">The _lclose function closes the specified file so that it is no longer available for reading or writing.</span></span> <span data-ttu-id="21bfb-110">Essa função é fornecida para compatibilidade com versões de 16 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="21bfb-110">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="21bfb-111">Os aplicativos baseados em Win32 devem usar a função CloseHandle.</span><span class="sxs-lookup"><span data-stu-id="21bfb-111">Win32-based applications should use the CloseHandle function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-113">A função _lopen abre um arquivo existente e define o ponteiro do arquivo para o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="21bfb-113">The _lopen function opens an existing file and sets the file pointer to the beginning of the file.</span></span> <span data-ttu-id="21bfb-114">Essa função é fornecida para compatibilidade com versões de 16 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="21bfb-114">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="21bfb-115">Os aplicativos baseados em Win32 devem usar a função CreateFile.</span><span class="sxs-lookup"><span data-stu-id="21bfb-115">Win32-based applications should use the CreateFile function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-117">A função _lread lê os dados do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="21bfb-117">The _lread function reads data from the specified file.</span></span> <span data-ttu-id="21bfb-118">Essa função é fornecida para compatibilidade com versões de 16 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="21bfb-118">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="21bfb-119">Os aplicativos baseados em Win32 devem usar a função ReadFile.</span><span class="sxs-lookup"><span data-stu-id="21bfb-119">Win32-based applications should use the ReadFile function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-121">Retorna um valor que indica se os codecs de DVD estão habilitados no dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="21bfb-121">Returns a value indicating whether DVD codecs are enabled on the current device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-123">Desabilita o recurso de fantasma da janela para o processo de chamada de GUI.</span><span class="sxs-lookup"><span data-stu-id="21bfb-123">Disables the window ghosting feature for the calling GUI process.</span></span> <span data-ttu-id="21bfb-124">O ghosting da janela é um recurso do Windows Manager que permite ao usuário minimizar, mover ou fechar a janela principal de um aplicativo que não está respondendo.</span><span class="sxs-lookup"><span data-stu-id="21bfb-124">Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-126">Retorna uma lista de propriedades para todos os codecs de mídia instalados no sistema que atendem aos requisitos especificados.</span><span class="sxs-lookup"><span data-stu-id="21bfb-126">Returns a list of properties for all media codecs installed on the system that meet the specified requirements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-128">Cria uma fábrica de comunicação para registrar uma extensão de mídia.</span><span class="sxs-lookup"><span data-stu-id="21bfb-128">Creates a communication factory for registering a media extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-130">Cria uma instância de uma classe em um pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="21bfb-130">Creates an instance of a class in an application package.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-132">Obtém um valor que indica se o comportamento de mídia associado ao GUID especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="21bfb-132">Gets a value indicating whether the media behavior associated with the specified GUID is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-134">Preterido.</span><span class="sxs-lookup"><span data-stu-id="21bfb-134">Deprecated.</span></span> <span data-ttu-id="21bfb-135">Essa função é usada para fechar o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="21bfb-135">This function is used to close the specified handle.</span></span> <span data-ttu-id="21bfb-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> é substituído por <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="21bfb-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> is superseded by <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-138">Preterido.</span><span class="sxs-lookup"><span data-stu-id="21bfb-138">Deprecated.</span></span> <span data-ttu-id="21bfb-139">Cria descritores para os buffers fornecidos e transmite os dados não tipados para o driver de dispositivo associado ao identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="21bfb-139">Builds descriptors for the supplied buffer(s) and passes the untyped data to the device driver associated with the file handle.</span></span> <span data-ttu-id="21bfb-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> é substituído por <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span><span class="sxs-lookup"><span data-stu-id="21bfb-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> is superseded by <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-142">Preterido.</span><span class="sxs-lookup"><span data-stu-id="21bfb-142">Deprecated.</span></span> <span data-ttu-id="21bfb-143">Aguarda até que o objeto especificado obtenha um estado de <code>signaled</code> .</span><span class="sxs-lookup"><span data-stu-id="21bfb-143">Waits until the specified object attains a state of <code>signaled</code>.</span></span> <span data-ttu-id="21bfb-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> é substituído por <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span><span class="sxs-lookup"><span data-stu-id="21bfb-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> is superseded by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-146">Converte a cadeia de caracteres de origem ANSI especificada em uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="21bfb-146">Converts the specified ANSI source string into a Unicode string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-148">Converte uma cadeia de caracteres em um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="21bfb-148">Converts a character string to an integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-150">Inicializa o buffer fornecido com uma representação de cadeia de caracteres do SID para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="21bfb-150">Initializes the supplied buffer with a string representation of the SID for the current user.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-152">Libera o buffer de cadeia de caracteres alocado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="21bfb-152">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-154">Libera o buffer de cadeia de caracteres alocado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="21bfb-154">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-156">Libera o buffer de cadeia de caracteres alocado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> ou por <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span><span class="sxs-lookup"><span data-stu-id="21bfb-156">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> or by <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-158">Inicializa uma cadeia de caracteres contada.</span><span class="sxs-lookup"><span data-stu-id="21bfb-158">Initializes a counted string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-160">Inicializa uma cadeia de caracteres Unicode contada.</span><span class="sxs-lookup"><span data-stu-id="21bfb-160">Initializes a counted Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-162">Converte a cadeia de caracteres de origem Unicode especificada em uma cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="21bfb-162">Converts the specified Unicode source string into an ANSI string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-164">Essa função converte a cadeia de caracteres de origem Unicode especificada em uma cadeia de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="21bfb-164">This functions converts the specified Unicode source string into an OEM string.</span></span> <span data-ttu-id="21bfb-165">A conversão é feita em relação à página de código OEM (OCP).</span><span class="sxs-lookup"><span data-stu-id="21bfb-165">The translation is done with respect to the OEM code page (OCP).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-167">Determina quantos bytes são necessários para representar uma cadeia de caracteres Unicode como uma cadeia de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="21bfb-167">Determines how many bytes are needed to represent a Unicode string as an ANSI string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-169">A função <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> converte a cadeia de caracteres Unicode especificada em uma nova cadeia de caracteres, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="21bfb-169">The <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> function translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-171">A função <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> converte a cadeia de caracteres de origem especificada em uma cadeia de caracteres Unicode, usando a página de código UTF-8.</span><span class="sxs-lookup"><span data-stu-id="21bfb-171">The <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> function translates the specified source string into a Unicode string, using the UTF-8 code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21bfb-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-173">Especifica uma ação ou processamento para o IME (editor de método de entrada) por meio de uma subfunção especificada.</span><span class="sxs-lookup"><span data-stu-id="21bfb-173">Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="21bfb-174">Esta função está obsoleta e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="21bfb-174">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21bfb-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="21bfb-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span></span></td>
<td><span data-ttu-id="21bfb-176">Habilita ou desabilita temporariamente um IME e, ao mesmo tempo, ativa ou desativa a exibição de todas as janelas pertencentes ao IME.</span><span class="sxs-lookup"><span data-stu-id="21bfb-176">Temporarily enables or disables an IME and, at the same time, turns on or off the display of all windows owned by the IME.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="21bfb-177">Esta função está obsoleta e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="21bfb-177">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a><span data-ttu-id="21bfb-178">Estruturas</span><span class="sxs-lookup"><span data-stu-id="21bfb-178">Structures</span></span>



| <span data-ttu-id="21bfb-179">Tópico</span><span class="sxs-lookup"><span data-stu-id="21bfb-179">Topic</span></span>                                 | <span data-ttu-id="21bfb-180">Sumário</span><span class="sxs-lookup"><span data-stu-id="21bfb-180">Contents</span></span>                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21bfb-181">**IMESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="21bfb-181">**IMESTRUCT**</span></span>](/windows/win32/api/ime/ns-ime-imestruct) | <span data-ttu-id="21bfb-182">Usado pelo [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) para especificar a subfunção a ser executada na mensagem do IME e seus parâmetros.</span><span class="sxs-lookup"><span data-stu-id="21bfb-182">Used by [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) to specify the subfunction to be executed in the IME message and its parameters.</span></span> <span data-ttu-id="21bfb-183">Essa estrutura também é usada para receber valores de retorno dessas subfunções.</span><span class="sxs-lookup"><span data-stu-id="21bfb-183">This structure is also used to receive return values from those subfunctions.</span></span><br/> |
| [<span data-ttu-id="21bfb-184">**Strings**</span><span class="sxs-lookup"><span data-stu-id="21bfb-184">**STRING**</span></span>](/windows/desktop/api/Winternl/ns-winternl-string)       | <span data-ttu-id="21bfb-185">Essa estrutura é usada com a função [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) .</span><span class="sxs-lookup"><span data-stu-id="21bfb-185">This structure is used with the [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) function.</span></span> <br/>                                                                                                              |



 

### <a name="compiler-routines"></a><span data-ttu-id="21bfb-186">Rotinas do compilador</span><span class="sxs-lookup"><span data-stu-id="21bfb-186">Compiler Routines</span></span>



| <span data-ttu-id="21bfb-187">Tópico</span><span class="sxs-lookup"><span data-stu-id="21bfb-187">Topic</span></span>                                                             | <span data-ttu-id="21bfb-188">Sumário</span><span class="sxs-lookup"><span data-stu-id="21bfb-188">Contents</span></span>                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21bfb-189">**\_\_\_Rotina de manipulador específico de C \_**</span><span class="sxs-lookup"><span data-stu-id="21bfb-189">**\_\_C\_specific\_handler Routine**</span></span>](--c-specific-handler2.md) | <span data-ttu-id="21bfb-190">O [**\_ \_ \_ \_ manipulador específico de c**](--c-specific-handler2.md) é uma rotina auxiliar para o compilador C.</span><span class="sxs-lookup"><span data-stu-id="21bfb-190">[**\_\_C\_specific\_handler**](--c-specific-handler2.md) is a helper routine for the C compiler.</span></span><br/> |
| [<span data-ttu-id="21bfb-191">\_Rotina alldiv</span><span class="sxs-lookup"><span data-stu-id="21bfb-191">\_alldiv Routine</span></span>](-win32-alldiv.md)                             | <span data-ttu-id="21bfb-192">a [ \_ rotina alldiv](-win32-alldiv.md) é uma rotina auxiliar para o compilador C.</span><span class="sxs-lookup"><span data-stu-id="21bfb-192">[\_alldiv Routine](-win32-alldiv.md) is a helper routine for the C compiler.</span></span><br/>                     |
| [<span data-ttu-id="21bfb-193">\_allmul</span><span class="sxs-lookup"><span data-stu-id="21bfb-193">\_allmul</span></span>](-win32-allmul.md) | <span data-ttu-id="21bfb-194">Multiplica dois **LONGLONG** ou **ULONGLONG**.</span><span class="sxs-lookup"><span data-stu-id="21bfb-194">Multiplies two **LONGLONG** or **ULONGLONG**.</span></span> |
| [<span data-ttu-id="21bfb-195">\_aulldiv</span><span class="sxs-lookup"><span data-stu-id="21bfb-195">\_aulldiv</span></span>](-win32-aulldiv.md) | <span data-ttu-id="21bfb-196">Divide dois inteiros **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="21bfb-196">Divides two **ULONGLONG** integers.</span></span> |
| [<span data-ttu-id="21bfb-197">\_Rotina chkstk</span><span class="sxs-lookup"><span data-stu-id="21bfb-197">\_chkstk Routine</span></span>](-win32-chkstk.md)                             | <span data-ttu-id="21bfb-198">a [ \_ rotina chkstk](-win32-chkstk.md) é uma rotina auxiliar para o compilador C.</span><span class="sxs-lookup"><span data-stu-id="21bfb-198">[\_chkstk Routine](-win32-chkstk.md) is a helper routine for the C compiler.</span></span><br/>                     |
