---
title: Tipos de Dados do Windows (BaseTsd.h)
description: Os tipos de dados com suporte pelo Windows são usados para definir valores de retorno de função, parâmetros de função e de mensagem e membros de estrutura.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- tipos de dados
- tipos de dados, Windows
- API do Windows
- API do Windows, tipos de dados
- APIENTRY
- ATOM
- BOOL
- BOOLEAN
- BYTE
- RETORNO
- CCHAR
- CHAR
- COLORREF
- CONST
- DWORD
- DWORDLONG
- DWORD_PTR
- DWORD32
- DWORD64
- FLOAT
- HACCEL
- HALF_PTR
- PROCESSAMENTO
- HBITMAP
- HBRUSH
- HCOLORSPACE
- HCONV
- HCONVLIST
- HCURSOR
- HDC
- HDDEDATA
- HDESK
- HDROP
- HDWP
- HENHMETAFILE
- HFILE
- HFONT
- HGDIOBJ
- HGLOBAL
- HHOOK
- HICON
- HINSTANCE
- HKEY
- HKL
- HLOCAL
- HMENU
- HMETAFILE
- HMODULE
- HMONITOR
- HPALETTE
- HPEN
- HRESULT
- HRGN
- HRSRC
- HSZ
- HWINSTA
- HWND
- INT
- INT_PTR
- INT8
- INT16
- INT32
- INT64
- LANGID
- LCID
- LCTYPE
- LGRPID
- LONG
- LONGLONG
- LONG_PTR
- LONG32
- LONG64
- LPARAM
- LPBOOL
- LPBYTE
- LPCOLORREF
- LPCSTR
- LPCTSTR
- LPCVOID
- LPCWSTR
- LPDWORD
- LPHANDLE
- LPINT
- LPLONG
- LPSTR
- LPTSTR
- LPVOID
- LPWORD
- LPWSTR
- LRESULT
- PBOOL
- PBOOLEAN
- PBYTE
- PCHAR
- PCSTR
- PCTSTR
- PCWSTR
- PDWORD
- PDWORDLONG
- PDWORD_PTR
- PDWORD32
- PDWORD64
- PFLOAT
- PHALF_PTR
- PHANDLE
- PHKEY
- APONTE
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- PLCID
- PLONG
- PLONGLONG
- PLONG_PTR
- PLONG32
- PLONG64
- POINTER_32
- POINTER_64
- POINTER_SIGNED
- POINTER_UNSIGNED
- PSHORT
- PSIZE_T
- PSSIZE_T
- PSTR
- PTBYTE
- PTCHAR
- PTSTR
- PUCHAR
- PUHALF_PTR
- PUINT
- PUINT_PTR
- PUINT8
- PUINT16
- PUINT32
- PUINT64
- PULONG
- PULONGLONG
- PULONG_PTR
- PULONG32
- PULONG64
- PUSHORT
- PVOID
- PWCHAR
- PWORD
- PWSTR
- QWORD
- SC_HANDLE
- SC_LOCK
- SERVICE_STATUS_HANDLE
- BAIXO
- SIZE_T
- SSIZE_T
- TBYTE
- TCHAR
- UCHAR
- UHALF_PTR
- UINT
- UINT_PTR
- UINT8
- UINT16
- UINT32
- UINT64
- ULONG
- ULONGLONG
- ULONG_PTR
- ULONG32
- ULONG64
- UNICODE_STRING
- NUM
- SEQÜÊNCIA
- LIVRE
- WCHAR
- WINAPI
- WORD
- WPARAM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf3a23e816a78f0dcae9c2fbd6e6979b936451c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369549"
---
# <a name="windows-data-types"></a>Tipos de dados do Windows

Os tipos de dados com suporte pelo Windows são usados para definir valores de retorno de função, parâmetros de função e de mensagem e membros de estrutura. Eles definem o tamanho e o significado desses elementos. Para obter mais informações sobre os tipos de dados do C/C++ subjacentes, consulte [intervalos de tipos de dados](/cpp/cpp/data-type-ranges?view=vs-2019).

A tabela a seguir contém os seguintes tipos: caractere, inteiro, booliano, ponteiro e identificador. Os tipos de caractere, inteiro e booliano são comuns à maioria dos compiladores de C. A maioria dos nomes de tipo de ponteiro começa com um prefixo de P ou LP. Os identificadores se referem a um recurso que foi carregado na memória.

Para obter mais informações sobre como lidar com inteiros de 64 bits, consulte [inteiros grandes](large-integers.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de dados</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></td>
<td>A Convenção de chamada para funções do sistema.<br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></td>
<td>Um Atom. Para obter mais informações, consulte <a href="/windows/desktop/dataxchg/about-atom-tables">sobre tabelas Atom</a>.<br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></td>
<td>Uma variável booliana (deve ser <strong>true</strong> ou <strong>false</strong>).<br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></td>
<td>Uma variável booliana (deve ser <strong>true</strong> ou <strong>false</strong>).<br/> Esse tipo é declarado em WinNT. h da seguinte maneira:<br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BYTE"></span><span id="byte"></span><strong>MINUCIOSA</strong></td>
<td>Um byte (8 bits).<br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CALLBACK"></span><span id="callback"></span><strong>RETORNO</strong></td>
<td>A Convenção de chamada para funções de retorno de chamada.<br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>#define CALLBACK __stdcall</code><br/> <strong>Retorno de chamada</strong>, <strong>Winapi tenha</strong>e <strong>APIENTRY</strong> são usados para definir funções com a Convenção de chamada __stdcall. A maioria das funções na API do Windows é declarada usando <strong>Winapi tenha</strong>. Talvez você queira usar o <strong>retorno de chamada</strong> para as funções de retorno de chamada implementadas para ajudar a identificar a função como uma função de retorno de chamada.<br/></td>
</tr>
<tr class="odd">
<td><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></td>
<td>Um caractere de 8 bits do Windows (ANSI).<br/> Esse tipo é declarado em WinNT. h da seguinte maneira:<br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CHAR"></span><span id="char"></span><strong>º</strong></td>
<td>Um caractere de 8 bits do Windows (ANSI). Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.<br/> Esse tipo é declarado em WinNT. h da seguinte maneira:<br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></td>
<td>O valor de cor vermelho, verde e azul (RGB) (32 bits). Consulte <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> para obter informações sobre esse tipo.<br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CONST"></span><span id="const"></span><strong>CONST</strong></td>
<td>Uma variável cujo valor deve permanecer constante durante a execução. <br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></td>
<td>Um inteiro sem sinal de 32 bits. O intervalo é de 0 a 4294967295 decimal.<br/> Esse tipo é declarado em IntSafe. h da seguinte maneira:<br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></td>
<td>Um inteiro sem sinal de 64 bits. O intervalo é de 0 a 18446744073709551615 decimal.<br/> Esse tipo é declarado em IntSafe. h da seguinte maneira:<br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></td>
<td>Um tipo longo sem sinal para a precisão do ponteiro. Use ao converter um ponteiro para um tipo longo para executar aritmética de ponteiro. (Também usado normalmente para parâmetros gerais de 32 bits que foram estendidos para 64 bits em janelas de 64 bits.)<br/> Esse tipo é declarado em BaseTsd. h da seguinte maneira:<br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></td>
<td>Um inteiro sem sinal de 32 bits.<br/> Esse tipo é declarado em BaseTsd. h da seguinte maneira:<br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></td>
<td>Um inteiro sem sinal de 64 bits.<br/> Esse tipo é declarado em BaseTsd. h da seguinte maneira:<br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span id="FLOAT"></span><span id="float"></span><strong>BARRA</strong></td>
<td>Uma variável de ponto flutuante.<br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></td>
<td>Um identificador para uma <a href="/windows/desktop/menurc/keyboard-accelerators">tabela de acelerador</a>.<br/> Esse tipo é declarado em WinDef. h da seguinte maneira:<br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></td>
<td>Metade do tamanho de um ponteiro. Use em uma estrutura que contém um ponteiro e dois campos pequenos.<br/> Esse tipo é declarado em BaseTsd. h da seguinte maneira:<br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef int HALF_PTR;
#else
 typedef short HALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span id="HANDLE"></span><span id="handle"></span><strong>PROCESSAMENTO</strong></td>
<td><p>Um identificador para um objeto.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/gdi/brushes">pincel</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></td>
<td><p>Um identificador para um <a href="/previous-versions//dd316799(v=vs.85)">espaço de cores</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></td>
<td><p>Um identificador para uma conversa de intercâmbio de dados dinâmicos (DDE).</p>
<p>Esse tipo é declarado em ddeml. h da seguinte maneira:</p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></td>
<td><p>Um identificador para uma lista de conversa DDE.</p>
<p>Esse tipo é declarado em ddeml. h da seguinte maneira:</p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/menurc/cursors">cursor</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/gdi/device-context-types">contexto de dispositivo</a> (DC).</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></td>
<td><p>Um identificador para dados DDE.</p>
<p>Esse tipo é declarado em ddeml. h da seguinte maneira:</p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></td>
<td><p>Um identificador para uma <a href="/windows/desktop/winstation/desktops">área de trabalho</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></td>
<td><p>Um identificador para uma estrutura de soltar interna.</p>
<p>Esse tipo é declarado em ShellApi. h da seguinte maneira:</p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></td>
<td><p>Um identificador para uma estrutura de posição de janela adiada.</p>
<p>Esse tipo é declarado em WinUser. h da seguinte maneira:</p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/gdi/metafiles">metarquivo avançado</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></td>
<td><p>Um identificador para um arquivo aberto pelo <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, não <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></td>
<td><p>Um identificador para uma <a href="/windows/desktop/gdi/about-fonts">fonte</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></td>
<td><p>Um identificador para um objeto GDI.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></td>
<td><p>Um identificador para um bloco de memória global.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/winmsg/hooks">gancho</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/menurc/icons">ícone</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></td>
<td><p>Um identificador para uma instância. Esse é o endereço base do módulo na memória.</p>
<p><strong>HMODULE</strong> e <strong>HINSTANCE</strong> são os mesmos hoje, mas representaram coisas diferentes no Windows de 16 bits.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></td>
<td><p>Um identificador para uma chave do registro.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></td>
<td><p>Um identificador de localidade de entrada.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></td>
<td><p>Um identificador para um bloco de memória local.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/menurc/menus">menu</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></td>
<td><p>Um identificador para um <a href="/windows/desktop/gdi/metafiles">metarquivo</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></td>
<td><p>Um identificador para um módulo. O é o endereço base do módulo na memória.</p>
<p><strong>HMODULE</strong> e <strong>HINSTANCE</strong> são os mesmos nas versões atuais do Windows, mas representaram coisas diferentes no Windows de 16 bits.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></td>
<td><p>Um identificador para um monitor de exibição.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></td>
<td><p>Um identificador para uma paleta.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></td>
<td><p>Um identificador para uma <a href="/windows/desktop/gdi/pens">caneta</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRESULT"></span><span id="hresult"></span><strong>RESULTADO</strong></td>
<td><p>Os códigos de retorno usados pelas interfaces COM. Para obter mais informações, consulte <a href="/windows/desktop/com/structure-of-com-error-codes">estrutura dos códigos de erro com</a>. Para testar um valor <strong>HRESULT</strong> , use as macros <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>com falha e com</strong></a> <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>êxito</strong></a> .</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></td>
<td><p>Um identificador para uma <a href="/windows/desktop/gdi/regions">região</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></td>
<td><p>Um identificador para um recurso.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></td>
<td><p>Um identificador para uma cadeia de caracteres DDE.</p>
<p>Esse tipo é declarado em ddeml. h da seguinte maneira:</p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></td>
<td><p>Um identificador para uma <a href="/windows/desktop/winstation/window-stations">estação de janela</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></td>
<td><p>Um identificador para uma <a href="/windows/desktop/winmsg/windows">janela</a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT"></span><span id="int"></span><strong>INTEIRO</strong></td>
<td><p>Um inteiro com sinal de 32 bits. O intervalo é de-2147483648 a 2147483647 decimal.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></td>
<td><p>Um tipo de inteiro assinado para precisão de ponteiro. Use ao converter um ponteiro para um inteiro para executar aritmética de ponteiro.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64) 
 typedef __int64 INT_PTR; 
#else 
 typedef int INT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></td>
<td><p>Um inteiro com sinal de 8 bits.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></td>
<td><p>Um inteiro de 16 bits com sinal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></td>
<td><p>Um inteiro com sinal de 32 bits. O intervalo é de-2147483648 a 2147483647 decimal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></td>
<td><p>Um inteiro com sinal de 64 bits. O intervalo é-9.223.372.036.854.775.808 até 9223372036854775807 decimal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></td>
<td><p>Um identificador de idioma. Para obter mais informações, consulte <a href="/windows/desktop/Intl/language-identifiers">identificadores de idioma</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></td>
<td><p>Um identificador de localidade. Para obter mais informações, consulte <a href="/windows/desktop/Intl/locale-identifiers">identificadores de localidade</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></td>
<td><p>Um tipo de informação de localidade. Para obter uma lista, consulte <a href="/windows/desktop/Intl/locale-information-constants">constantes de informações de localidade</a>.</p>
<p>Esse tipo é declarado em WinNls. h da seguinte maneira:</p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></td>
<td><p>Um identificador de grupo de idiomas. Para obter uma lista, consulte <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</p>
<p>Esse tipo é declarado em WinNls. h da seguinte maneira:</p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG"></span><span id="long"></span><strong>Longas</strong></td>
<td><p>Um inteiro com sinal de 32 bits. O intervalo é de-2147483648 a 2147483647 decimal.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></td>
<td><p>Um inteiro com sinal de 64 bits. O intervalo é-9.223.372.036.854.775.808 até 9223372036854775807 decimal.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef __int64 LONGLONG; 
#else
 typedef double LONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></td>
<td><p>Um tipo longo assinado para a precisão do ponteiro. Use ao converter um ponteiro para um longo para executar a aritmética do ponteiro.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef __int64 LONG_PTR; 
#else
 typedef long LONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></td>
<td><p>Um inteiro com sinal de 32 bits. O intervalo é de-2147483648 a 2147483647 decimal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></td>
<td><p>Um inteiro com sinal de 64 bits. O intervalo é-9.223.372.036.854.775.808 até 9223372036854775807 decimal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></td>
<td><p>Um parâmetro de mensagem.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></td>
<td><p>Um ponteiro para um <a href="#bool"><strong>bool</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></td>
<td><p>Um ponteiro para um <a href="#byte"><strong>byte</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></td>
<td><p>Um ponteiro para um valor de <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></td>
<td><p>Um ponteiro para uma cadeia de caracteres constante terminada em nulo de caracteres ANSI (Windows de 8 bits). Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></td>
<td><p>Um <a href="#lpcwstr"><strong>LPCWSTR</strong></a> se <strong>Unicode</strong> estiver definido; caso contrário, <a href="#lpcstr"><strong>LPCSTR</strong></a> . Para obter mais informações, consulte <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de dados do Windows para cadeias de caracteres</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR LPCTSTR; 
#else
 typedef LPCSTR LPCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></td>
<td><p>Um ponteiro para uma constante de qualquer tipo.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></td>
<td><p>Um ponteiro para uma cadeia de caracteres constante terminada em nulo de caracteres Unicode de 16 bits. Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></td>
<td><p>Um ponteiro para um <a href="#dword"><strong>DWORD</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></td>
<td><p>Um ponteiro para um <a href="#handle"><strong>identificador</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></td>
<td><p>Um ponteiro para um <a href="#int"><strong>int</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></td>
<td><p>Um ponteiro para um <a href="#long"><strong>longo</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></td>
<td><p>Um ponteiro para uma cadeia de caracteres do Windows de 8 bits terminada por nulo. Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></td>
<td><p>Um <a href="#lpwstr"><strong>LPWSTR</strong></a> se o <strong>Unicode</strong> for definido, um <a href="#lpstr"><strong>LPSTR</strong></a> , caso contrário. Para obter mais informações, consulte <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de dados do Windows para cadeias de caracteres</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR LPTSTR;
#else
 typedef LPSTR LPTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></td>
<td><p>Um ponteiro para qualquer tipo.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></td>
<td><p>Um ponteiro para uma <a href="#word"><strong>palavra</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></td>
<td><p>Um ponteiro para uma cadeia de caracteres Unicode de 16 bits terminada em nulo. Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></td>
<td><p>Resultado assinado do processamento de mensagens.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></td>
<td><p>Um ponteiro para um <a href="#bool"><strong>bool</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></td>
<td><p>Um ponteiro para um <a href="#boolean"><strong>booliano</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></td>
<td><p>Um ponteiro para um <a href="#byte"><strong>byte</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></td>
<td><p>Um ponteiro para um <a href="#char"><strong>Char</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></td>
<td><p>Um ponteiro para uma cadeia de caracteres constante terminada em nulo de caracteres ANSI (Windows de 8 bits). Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></td>
<td><p>Um <a href="#pcwstr"><strong>PCWSTR</strong></a> se o <strong>Unicode</strong> estiver definido; caso contrário, <a href="#pcstr"><strong>PCSTR</strong></a> . Para obter mais informações, consulte <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de dados do Windows para cadeias de caracteres</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR PCTSTR;
#else
 typedef LPCSTR PCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></td>
<td><p>Um ponteiro para uma cadeia de caracteres constante terminada em nulo de caracteres Unicode de 16 bits. Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></td>
<td><p>Um ponteiro para um <a href="#dword"><strong>DWORD</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></td>
<td><p>Um ponteiro para um <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></td>
<td><p>Um ponteiro para um <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></td>
<td><p>Um ponteiro para um <a href="#dword32"><strong>DWORD32</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></td>
<td><p>Um ponteiro para um <a href="#dword64"><strong>DWORD64</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></td>
<td><p>Um ponteiro para um <a href="#float"><strong>float</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></td>
<td><p>Um ponteiro para um <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef HALF_PTR *PHALF_PTR;
#else
 typedef HALF_PTR *PHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></td>
<td><p>Um ponteiro para um <a href="#handle"><strong>identificador</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></td>
<td><p>Um ponteiro para um <a href="#hkey"><strong>HKEY</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT"></span><span id="pint"></span><strong>APONTE</strong></td>
<td><p>Um ponteiro para um <a href="#int"><strong>int</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></td>
<td><p>Um ponteiro para um <a href="#int_ptr"><strong>INT_PTR</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></td>
<td><p>Um ponteiro para um <a href="#int8"><strong>INT8</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></td>
<td><p>Um ponteiro para um <a href="#int16"><strong>Int16</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></td>
<td><p>Um ponteiro para um <a href="#int32"><strong>INT32</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></td>
<td><p>Um ponteiro para um <a href="#int64"><strong>Int64</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></td>
<td><p>Um ponteiro para um <a href="#lcid"><strong>LCID</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></td>
<td><p>Um ponteiro para um <a href="#long"><strong>longo</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></td>
<td><p>Um ponteiro para um <a href="#longlong"><strong>LONGLONG</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></td>
<td><p>Um ponteiro para um <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></td>
<td><p>Um ponteiro para um <a href="#long32"><strong>LONG32</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></td>
<td><p>Um ponteiro para um <a href="#long64"><strong>LONG64</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></td>
<td><p>Um ponteiro de 32 bits. Em um sistema de 32 bits, esse é um ponteiro nativo. Em um sistema de 64 bits, esse é um ponteiro de bit de 64 truncado.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
#define POINTER_32 __ptr32
#else
#define POINTER_32
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></td>
<td><p>Um ponteiro de 64 bits. Em um sistema de 64 bits, esse é um ponteiro nativo. Em um sistema de 32 bits, esse é um ponteiro de bit de 32 de sinal estendido.</p>
<p>Observe que não é seguro assumir o estado do bit de ponteiro alto.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if (_MSC_VER >= 1300)
#define POINTER_64 __ptr64
#else
#define POINTER_64
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></td>
<td><p>Um ponteiro assinado.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></td>
<td><p>Um ponteiro não assinado.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></td>
<td><p>Um ponteiro para um <a href="#short"><strong>curto</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></td>
<td><p>Um ponteiro para um <a href="#size_t"><strong>size_t</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></td>
<td><p>Um ponteiro para um <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></td>
<td><p>Um ponteiro para uma cadeia de caracteres do Windows de 8 bits terminada por nulo. Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></td>
<td><p>Um ponteiro para um <a href="#tbyte"><strong>Tbyte</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></td>
<td><p>Um ponteiro para um <a href="#tchar"><strong>TCHAR</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></td>
<td><p>Um <a href="#pwstr"><strong>PWSTR</strong></a> se o <strong>Unicode</strong> estiver definido; caso contrário, <a href="#pstr"><strong>PSTR</strong></a> . Para obter mais informações, consulte <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de dados do Windows para cadeias de caracteres</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR PTSTR;
#else typedef LPSTR PTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></td>
<td><p>Um ponteiro para um <a href="#uchar"><strong>UCHAR</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></td>
<td><p>Um ponteiro para um <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef UHALF_PTR *PUHALF_PTR;
#else
 typedef UHALF_PTR *PUHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></td>
<td><p>Um ponteiro para um <a href="#uint"><strong>uint</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></td>
<td><p>Um ponteiro para um <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></td>
<td><p>Um ponteiro para um <a href="#uint8"><strong>UINT8</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></td>
<td><p>Um ponteiro para um <a href="#uint16"><strong>UINT16</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></td>
<td><p>Um ponteiro para um <a href="#uint32"><strong>UINT32</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></td>
<td><p>Um ponteiro para um <a href="#uint64"><strong>UINT64</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></td>
<td><p>Um ponteiro para um <a href="#ulong"><strong>ULONG</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></td>
<td><p>Um ponteiro para um <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></td>
<td><p>Um ponteiro para um <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></td>
<td><p>Um ponteiro para um <a href="#ulong32"><strong>ULONG32</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></td>
<td><p>Um ponteiro para um <a href="#ulong64"><strong>ULONG64</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></td>
<td><p>Um ponteiro para um <a href="#ushort"><strong>UShort</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></td>
<td><p>Um ponteiro para qualquer tipo.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></td>
<td><p>Um ponteiro para um <a href="#wchar"><strong>WCHAR</strong></a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></td>
<td><p>Um ponteiro para uma <a href="#word"><strong>palavra</strong></a>.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></td>
<td><p>Um ponteiro para uma cadeia de caracteres Unicode de 16 bits terminada em nulo. Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></td>
<td><p>Um inteiro sem sinal de 64 bits.</p>
<p>Esse tipo é declarado da seguinte maneira:</p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></td>
<td><p>Um identificador para um banco de dados do Gerenciador de controle de serviço. Para obter mais informações, consulte <a href="/windows/desktop/Services/scm-handles">identificadores SCM</a>.</p>
<p>Esse tipo é declarado em WinSvc. h da seguinte maneira:</p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></td>
<td><p>Um bloqueio para um banco de dados do Gerenciador de controle de serviço. Para obter mais informações, consulte <a href="/windows/desktop/Services/scm-handles">identificadores SCM</a>.</p>
<p>Esse tipo é declarado em WinSvc. h da seguinte maneira:</p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></td>
<td><p>Um identificador para um valor de status de serviço. Para obter mais informações, consulte <a href="/windows/desktop/Services/scm-handles">identificadores SCM</a>.</p>
<p>Esse tipo é declarado em WinSvc. h da seguinte maneira:</p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SHORT"></span><span id="short"></span><strong>BAIXO</strong></td>
<td><p>Um inteiro de 16 bits. O intervalo é de-32768 a 32767 decimal.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></td>
<td><p>O número máximo de bytes aos quais um ponteiro pode apontar. Use para uma contagem que deve abranger o intervalo completo de um ponteiro.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></td>
<td><p>Uma versão assinada do <a href="#size_t"><strong>size_t</strong></a>.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></td>
<td><p>Um <a href="#char"><strong>caractere</strong></a> <a href="#wchar"><strong>WCHAR</strong></a> se <strong>Unicode</strong> estiver definido, caso contrário.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TBYTE;
#else
 typedef unsigned char TBYTE;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></td>
<td><p>Um <a href="#char"><strong>caractere</strong></a> <a href="#wchar"><strong>WCHAR</strong></a> se <strong>Unicode</strong> estiver definido, caso contrário.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TCHAR;
#else
 typedef char TCHAR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></td>
<td><p>Um <a href="#char"><strong>Char</strong></a>não assinado.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></td>
<td><p>Um <a href="#half_ptr"><strong>HALF_PTR</strong></a>não assinado. Use em uma estrutura que contém um ponteiro e dois campos pequenos.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef unsigned int UHALF_PTR;
#else
 typedef unsigned short UHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></td>
<td><p>Um <a href="#int"><strong>int</strong></a>não assinado. O intervalo é de 0 a 4294967295 decimal.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></td>
<td><p>Um <a href="#int_ptr"><strong>INT_PTR</strong></a>não assinado.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 UINT_PTR;
#else
 typedef unsigned int UINT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></td>
<td><p>Um <a href="#int8"><strong>INT8</strong></a>não assinado.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></td>
<td><p>Um <a href="#int16"><strong>Int16</strong></a>não assinado.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></td>
<td><p>Um <a href="#int32"><strong>INT32</strong></a>não assinado. O intervalo é de 0 a 4294967295 decimal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></td>
<td><p>Um <a href="#int64"><strong>Int64</strong></a>não assinado. O intervalo é de 0 a 18446744073709551615 decimal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></td>
<td><p>Um <a href="#long"><strong>longo</strong></a>não assinado. O intervalo é de 0 a 4294967295 decimal.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></td>
<td><p>Um inteiro sem sinal de 64 bits. O intervalo é de 0 a 18446744073709551615 decimal.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef unsigned __int64 ULONGLONG;
#else
 typedef double ULONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></td>
<td><p>Um <a href="#long_ptr"><strong>LONG_PTR</strong></a>não assinado.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 ULONG_PTR;
#else
 typedef unsigned long ULONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></td>
<td><p>Um <a href="#long32"><strong>LONG32</strong></a>não assinado. O intervalo é de 0 a 4294967295 decimal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></td>
<td><p>Um <a href="#long64"><strong>LONG64</strong></a>não assinado. O intervalo é de 0 a 18446744073709551615 decimal.</p>
<p>Esse tipo é declarado em BaseTsd. h da seguinte maneira:</p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></td>
<td><p>Uma cadeia de caracteres Unicode.</p>
<p>Esse tipo é declarado em Winternl. h da seguinte maneira:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>typedef struct _UNICODE_STRING {
  USHORT  Length;
  USHORT  MaximumLength;
  PWSTR  Buffer;
} UNICODE_STRING;
typedef UNICODE_STRING *PUNICODE_STRING;
typedef const UNICODE_STRING *PCUNICODE_STRING;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="USHORT"></span><span id="ushort"></span><strong>NUM</strong></td>
<td><p>Um <a href="#short"><strong>curto</strong></a>não assinado. O intervalo é de 0 a 65535 decimal.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="USN"></span><span id="usn"></span><strong>SEQÜÊNCIA</strong></td>
<td><p>Um USN (número de sequência de atualização).</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="VOID"></span><span id="void"></span><strong>LIVRE</strong></td>
<td><p>Qualquer tipo.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></td>
<td><p>Um caractere Unicode de 16 bits. Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</p>
<p>Esse tipo é declarado em WinNT. h da seguinte maneira:</p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WINAPI"></span><span id="winapi"></span><strong>Winapi tenha</strong></td>
<td><p>A Convenção de chamada para funções do sistema.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>#define WINAPI __stdcall</code></p>
<p><strong>Retorno de chamada</strong>, <strong>Winapi tenha</strong>e <strong>APIENTRY</strong> são usados para definir funções com a Convenção de chamada __stdcall. A maioria das funções na API do Windows é declarada usando <strong>Winapi tenha</strong>. Talvez você queira usar o <strong>retorno de chamada</strong> para as funções de retorno de chamada implementadas para ajudar a identificar a função como uma função de retorno de chamada.</p></td>
</tr>
<tr class="even">
<td><span id="WORD"></span><span id="word"></span><strong>TEXTOS</strong></td>
<td><p>Um inteiro sem sinal de 16 bits. O intervalo é de 0 a 65535 decimal.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></td>
<td><p>Um parâmetro de mensagem.</p>
<p>Esse tipo é declarado em WinDef. h da seguinte maneira:</p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                                                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>BaseTsd. h; </dt> <dt>WinDef. h; </dt> <dt>Winnt. h</dt> </dl> |
