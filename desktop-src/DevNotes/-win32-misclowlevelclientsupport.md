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
# <a name="miscellaneous-low-level-client-support"></a>Suporte de cliente variado Low-Level

Este tópico contém informações sobre APIs de nível baixo que são usadas pela infraestrutura de cliente do Windows.

### <a name="functions"></a>Funções



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Sumário</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></td>
<td>A função _lclose fecha o arquivo especificado para que ele não fique mais disponível para leitura ou gravação. Essa função é fornecida para compatibilidade com versões de 16 bits do Windows. Os aplicativos baseados em Win32 devem usar a função CloseHandle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></td>
<td>A função _lopen abre um arquivo existente e define o ponteiro do arquivo para o início do arquivo. Essa função é fornecida para compatibilidade com versões de 16 bits do Windows. Os aplicativos baseados em Win32 devem usar a função CreateFile. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></td>
<td>A função _lread lê os dados do arquivo especificado. Essa função é fornecida para compatibilidade com versões de 16 bits do Windows. Os aplicativos baseados em Win32 devem usar a função ReadFile. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></td>
<td>Retorna um valor que indica se os codecs de DVD estão habilitados no dispositivo atual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></td>
<td>Desabilita o recurso de fantasma da janela para o processo de chamada de GUI. O ghosting da janela é um recurso do Windows Manager que permite ao usuário minimizar, mover ou fechar a janela principal de um aplicativo que não está respondendo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></td>
<td>Retorna uma lista de propriedades para todos os codecs de mídia instalados no sistema que atendem aos requisitos especificados.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></td>
<td>Cria uma fábrica de comunicação para registrar uma extensão de mídia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></td>
<td>Cria uma instância de uma classe em um pacote de aplicativos. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></td>
<td>Obtém um valor que indica se o comportamento de mídia associado ao GUID especificado está habilitado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></td>
<td>Preterido. Essa função é usada para fechar o identificador especificado. <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> é substituído por <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></td>
<td>Preterido. Cria descritores para os buffers fornecidos e transmite os dados não tipados para o driver de dispositivo associado ao identificador de arquivo. <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> é substituído por <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></td>
<td>Preterido. Aguarda até que o objeto especificado obtenha um estado de <code>signaled</code> . <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> é substituído por <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></td>
<td>Converte a cadeia de caracteres de origem ANSI especificada em uma cadeia de caracteres Unicode. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></td>
<td>Converte uma cadeia de caracteres em um número inteiro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></td>
<td>Inicializa o buffer fornecido com uma representação de cadeia de caracteres do SID para o usuário atual. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></td>
<td>Libera o buffer de cadeia de caracteres alocado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></td>
<td>Libera o buffer de cadeia de caracteres alocado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></td>
<td>Libera o buffer de cadeia de caracteres alocado por <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> ou por <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></td>
<td>Inicializa uma cadeia de caracteres contada. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></td>
<td>Inicializa uma cadeia de caracteres Unicode contada. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></td>
<td>Converte a cadeia de caracteres de origem Unicode especificada em uma cadeia de caracteres ANSI. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></td>
<td>Essa função converte a cadeia de caracteres de origem Unicode especificada em uma cadeia de caracteres OEM. A conversão é feita em relação à página de código OEM (OCP). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></td>
<td>Determina quantos bytes são necessários para representar uma cadeia de caracteres Unicode como uma cadeia de caracteres ANSI.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></td>
<td>A função <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> converte a cadeia de caracteres Unicode especificada em uma nova cadeia de caracteres, usando a página de código UTF-8 (Unicode Transformation Format) de 8 bits.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></td>
<td>A função <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> converte a cadeia de caracteres de origem especificada em uma cadeia de caracteres Unicode, usando a página de código UTF-8.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></td>
<td>Especifica uma ação ou processamento para o IME (editor de método de entrada) por meio de uma subfunção especificada.
<blockquote>
[!Note]<br />
Esta função está obsoleta e não deve ser usada.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></td>
<td>Habilita ou desabilita temporariamente um IME e, ao mesmo tempo, ativa ou desativa a exibição de todas as janelas pertencentes ao IME.
<blockquote>
[!Note]<br />
Esta função está obsoleta e não deve ser usada.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Estruturas



| Tópico                                 | Sumário                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMESTRUCT**](/windows/win32/api/ime/ns-ime-imestruct) | Usado pelo [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) para especificar a subfunção a ser executada na mensagem do IME e seus parâmetros. Essa estrutura também é usada para receber valores de retorno dessas subfunções.<br/> |
| [**Strings**](/windows/desktop/api/Winternl/ns-winternl-string)       | Essa estrutura é usada com a função [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) . <br/>                                                                                                              |



 

### <a name="compiler-routines"></a>Rotinas do compilador



| Tópico                                                             | Sumário                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_\_\_Rotina de manipulador específico de C \_**](--c-specific-handler2.md) | O [**\_ \_ \_ \_ manipulador específico de c**](--c-specific-handler2.md) é uma rotina auxiliar para o compilador C.<br/> |
| [\_Rotina alldiv](-win32-alldiv.md)                             | a [ \_ rotina alldiv](-win32-alldiv.md) é uma rotina auxiliar para o compilador C.<br/>                     |
| [\_allmul](-win32-allmul.md) | Multiplica dois **LONGLONG** ou **ULONGLONG**. |
| [\_aulldiv](-win32-aulldiv.md) | Divide dois inteiros **ULONGLONG** . |
| [\_Rotina chkstk](-win32-chkstk.md)                             | a [ \_ rotina chkstk](-win32-chkstk.md) é uma rotina auxiliar para o compilador C.<br/>                     |
