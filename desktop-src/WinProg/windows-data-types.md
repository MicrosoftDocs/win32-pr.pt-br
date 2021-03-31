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
# <a name="windows-data-types"></a><span data-ttu-id="37b6c-280">Tipos de dados do Windows</span><span class="sxs-lookup"><span data-stu-id="37b6c-280">Windows Data Types</span></span>

<span data-ttu-id="37b6c-281">Os tipos de dados com suporte pelo Windows são usados para definir valores de retorno de função, parâmetros de função e de mensagem e membros de estrutura.</span><span class="sxs-lookup"><span data-stu-id="37b6c-281">The data types supported by Windows are used to define function return values, function and message parameters, and structure members.</span></span> <span data-ttu-id="37b6c-282">Eles definem o tamanho e o significado desses elementos.</span><span class="sxs-lookup"><span data-stu-id="37b6c-282">They define the size and meaning of these elements.</span></span> <span data-ttu-id="37b6c-283">Para obter mais informações sobre os tipos de dados do C/C++ subjacentes, consulte [intervalos de tipos de dados](/cpp/cpp/data-type-ranges?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="37b6c-283">For more information about the underlying C/C++ data types, see [Data Type Ranges](/cpp/cpp/data-type-ranges?view=vs-2019).</span></span>

<span data-ttu-id="37b6c-284">A tabela a seguir contém os seguintes tipos: caractere, inteiro, booliano, ponteiro e identificador.</span><span class="sxs-lookup"><span data-stu-id="37b6c-284">The following table contains the following types: character, integer, Boolean, pointer, and handle.</span></span> <span data-ttu-id="37b6c-285">Os tipos de caractere, inteiro e booliano são comuns à maioria dos compiladores de C.</span><span class="sxs-lookup"><span data-stu-id="37b6c-285">The character, integer, and Boolean types are common to most C compilers.</span></span> <span data-ttu-id="37b6c-286">A maioria dos nomes de tipo de ponteiro começa com um prefixo de P ou LP.</span><span class="sxs-lookup"><span data-stu-id="37b6c-286">Most of the pointer-type names begin with a prefix of P or LP.</span></span> <span data-ttu-id="37b6c-287">Os identificadores se referem a um recurso que foi carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="37b6c-287">Handles refer to a resource that has been loaded into memory.</span></span>

<span data-ttu-id="37b6c-288">Para obter mais informações sobre como lidar com inteiros de 64 bits, consulte [inteiros grandes](large-integers.md).</span><span class="sxs-lookup"><span data-stu-id="37b6c-288">For more information about handling 64-bit integers, see [Large Integers](large-integers.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-289">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="37b6c-289">Data type</span></span></th>
<th><span data-ttu-id="37b6c-290">Descrição</span><span class="sxs-lookup"><span data-stu-id="37b6c-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37b6c-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span></span></td>
<td><span data-ttu-id="37b6c-292">A Convenção de chamada para funções do sistema.</span><span class="sxs-lookup"><span data-stu-id="37b6c-292">The calling convention for system functions.</span></span><br/> <span data-ttu-id="37b6c-293">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-293">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span></span></td>
<td><span data-ttu-id="37b6c-295">Um Atom.</span><span class="sxs-lookup"><span data-stu-id="37b6c-295">An atom.</span></span> <span data-ttu-id="37b6c-296">Para obter mais informações, consulte <a href="/windows/desktop/dataxchg/about-atom-tables">sobre tabelas Atom</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-296">For more information, see <a href="/windows/desktop/dataxchg/about-atom-tables">About Atom Tables</a>.</span></span><br/> <span data-ttu-id="37b6c-297">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-297">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span></span></td>
<td><span data-ttu-id="37b6c-299">Uma variável booliana (deve ser <strong>true</strong> ou <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="37b6c-299">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="37b6c-300">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-300">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span></span></td>
<td><span data-ttu-id="37b6c-302">Uma variável booliana (deve ser <strong>true</strong> ou <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="37b6c-302">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="37b6c-303">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-303">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-304"><span id="BYTE"></span><span id="byte"></span><strong>MINUCIOSA</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></span></span></td>
<td><span data-ttu-id="37b6c-305">Um byte (8 bits).</span><span class="sxs-lookup"><span data-stu-id="37b6c-305">A byte (8 bits).</span></span><br/> <span data-ttu-id="37b6c-306">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-306">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-307"><span id="CALLBACK"></span><span id="callback"></span><strong>RETORNO</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-307"><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></span></span></td>
<td><span data-ttu-id="37b6c-308">A Convenção de chamada para funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="37b6c-308">The calling convention for callback functions.</span></span><br/> <span data-ttu-id="37b6c-309">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-309">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CALLBACK __stdcall</code><br/> <span data-ttu-id="37b6c-310"><strong>Retorno de chamada</strong>, <strong>Winapi tenha</strong>e <strong>APIENTRY</strong> são usados para definir funções com a Convenção de chamada __stdcall.</span><span class="sxs-lookup"><span data-stu-id="37b6c-310"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="37b6c-311">A maioria das funções na API do Windows é declarada usando <strong>Winapi tenha</strong>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-311">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="37b6c-312">Talvez você queira usar o <strong>retorno de chamada</strong> para as funções de retorno de chamada implementadas para ajudar a identificar a função como uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="37b6c-312">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span></span></td>
<td><span data-ttu-id="37b6c-314">Um caractere de 8 bits do Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="37b6c-314">An 8-bit Windows (ANSI) character.</span></span><br/> <span data-ttu-id="37b6c-315">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-315">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-316"><span id="CHAR"></span><span id="char"></span><strong>º</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span></span></td>
<td><span data-ttu-id="37b6c-317">Um caractere de 8 bits do Windows (ANSI).</span><span class="sxs-lookup"><span data-stu-id="37b6c-317">An 8-bit Windows (ANSI) character.</span></span> <span data-ttu-id="37b6c-318">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-318">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span><br/> <span data-ttu-id="37b6c-319">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-319">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span></span></td>
<td><span data-ttu-id="37b6c-321">O valor de cor vermelho, verde e azul (RGB) (32 bits).</span><span class="sxs-lookup"><span data-stu-id="37b6c-321">The red, green, blue (RGB) color value (32 bits).</span></span> <span data-ttu-id="37b6c-322">Consulte <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> para obter informações sobre esse tipo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-322">See <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> for information on this type.</span></span><br/> <span data-ttu-id="37b6c-323">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-323">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span></span></td>
<td><span data-ttu-id="37b6c-325">Uma variável cujo valor deve permanecer constante durante a execução.</span><span class="sxs-lookup"><span data-stu-id="37b6c-325">A variable whose value is to remain constant during execution.</span></span> <br/> <span data-ttu-id="37b6c-326">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-326">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="37b6c-328">Um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-328">A 32-bit unsigned integer.</span></span> <span data-ttu-id="37b6c-329">O intervalo é de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-329">The range is 0 through 4294967295 decimal.</span></span><br/> <span data-ttu-id="37b6c-330">Esse tipo é declarado em IntSafe. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-330">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span></span></td>
<td><span data-ttu-id="37b6c-332">Um inteiro sem sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-332">A 64-bit unsigned integer.</span></span> <span data-ttu-id="37b6c-333">O intervalo é de 0 a 18446744073709551615 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-333">The range is 0 through 18446744073709551615 decimal.</span></span><br/> <span data-ttu-id="37b6c-334">Esse tipo é declarado em IntSafe. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-334">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span></span></td>
<td><span data-ttu-id="37b6c-336">Um tipo longo sem sinal para a precisão do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-336">An unsigned long type for pointer precision.</span></span> <span data-ttu-id="37b6c-337">Use ao converter um ponteiro para um tipo longo para executar aritmética de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-337">Use when casting a pointer to a long type to perform pointer arithmetic.</span></span> <span data-ttu-id="37b6c-338">(Também usado normalmente para parâmetros gerais de 32 bits que foram estendidos para 64 bits em janelas de 64 bits.)</span><span class="sxs-lookup"><span data-stu-id="37b6c-338">(Also commonly used for general 32-bit parameters that have been extended to 64 bits in 64-bit Windows.)</span></span><br/> <span data-ttu-id="37b6c-339">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-339">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span></span></td>
<td><span data-ttu-id="37b6c-341">Um inteiro sem sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-341">A 32-bit unsigned integer.</span></span><br/> <span data-ttu-id="37b6c-342">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-342">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span></span></td>
<td><span data-ttu-id="37b6c-344">Um inteiro sem sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-344">A 64-bit unsigned integer.</span></span><br/> <span data-ttu-id="37b6c-345">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-345">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-346"><span id="FLOAT"></span><span id="float"></span><strong>BARRA</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOAT</strong></span></span></td>
<td><span data-ttu-id="37b6c-347">Uma variável de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="37b6c-347">A floating-point variable.</span></span><br/> <span data-ttu-id="37b6c-348">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-348">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span></span></td>
<td><span data-ttu-id="37b6c-350">Um identificador para uma <a href="/windows/desktop/menurc/keyboard-accelerators">tabela de acelerador</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-350">A handle to an <a href="/windows/desktop/menurc/keyboard-accelerators">accelerator table</a>.</span></span><br/> <span data-ttu-id="37b6c-351">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-351">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span></span></td>
<td><span data-ttu-id="37b6c-353">Metade do tamanho de um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-353">Half the size of a pointer.</span></span> <span data-ttu-id="37b6c-354">Use em uma estrutura que contém um ponteiro e dois campos pequenos.</span><span class="sxs-lookup"><span data-stu-id="37b6c-354">Use within a structure that contains a pointer and two small fields.</span></span><br/> <span data-ttu-id="37b6c-355">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-355">This type is declared in BaseTsd.h as follows:</span></span><br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-356">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-356">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-357"><span id="HANDLE"></span><span id="handle"></span><strong>PROCESSAMENTO</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-357"><span id="HANDLE"></span><span id="handle"></span><strong>HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-358">Um identificador para um objeto.</span><span class="sxs-lookup"><span data-stu-id="37b6c-358">A handle to an object.</span></span></p>
<p><span data-ttu-id="37b6c-359">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-359">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-361">Um identificador para um <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-361">A handle to a <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span></span></p>
<p><span data-ttu-id="37b6c-362">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-362">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-364">Um identificador para um <a href="/windows/desktop/gdi/brushes">pincel</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-364">A handle to a <a href="/windows/desktop/gdi/brushes">brush</a>.</span></span></p>
<p><span data-ttu-id="37b6c-365">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-365">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-367">Um identificador para um <a href="/previous-versions//dd316799(v=vs.85)">espaço de cores</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-367">A handle to a <a href="/previous-versions//dd316799(v=vs.85)">color space</a>.</span></span></p>
<p><span data-ttu-id="37b6c-368">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-368">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-370">Um identificador para uma conversa de intercâmbio de dados dinâmicos (DDE).</span><span class="sxs-lookup"><span data-stu-id="37b6c-370">A handle to a dynamic data exchange (DDE) conversation.</span></span></p>
<p><span data-ttu-id="37b6c-371">Esse tipo é declarado em ddeml. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-371">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-373">Um identificador para uma lista de conversa DDE.</span><span class="sxs-lookup"><span data-stu-id="37b6c-373">A handle to a DDE conversation list.</span></span></p>
<p><span data-ttu-id="37b6c-374">Esse tipo é declarado em ddeml. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-374">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-376">Um identificador para um <a href="/windows/desktop/menurc/cursors">cursor</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-376">A handle to a <a href="/windows/desktop/menurc/cursors">cursor</a>.</span></span></p>
<p><span data-ttu-id="37b6c-377">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-377">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-379">Um identificador para um <a href="/windows/desktop/gdi/device-context-types">contexto de dispositivo</a> (DC).</span><span class="sxs-lookup"><span data-stu-id="37b6c-379">A handle to a <a href="/windows/desktop/gdi/device-context-types">device context</a> (DC).</span></span></p>
<p><span data-ttu-id="37b6c-380">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-380">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-382">Um identificador para dados DDE.</span><span class="sxs-lookup"><span data-stu-id="37b6c-382">A handle to DDE data.</span></span></p>
<p><span data-ttu-id="37b6c-383">Esse tipo é declarado em ddeml. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-383">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-385">Um identificador para uma <a href="/windows/desktop/winstation/desktops">área de trabalho</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-385">A handle to a <a href="/windows/desktop/winstation/desktops">desktop</a>.</span></span></p>
<p><span data-ttu-id="37b6c-386">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-386">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-388">Um identificador para uma estrutura de soltar interna.</span><span class="sxs-lookup"><span data-stu-id="37b6c-388">A handle to an internal drop structure.</span></span></p>
<p><span data-ttu-id="37b6c-389">Esse tipo é declarado em ShellApi. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-389">This type is declared in ShellApi.h as follows:</span></span></p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-391">Um identificador para uma estrutura de posição de janela adiada.</span><span class="sxs-lookup"><span data-stu-id="37b6c-391">A handle to a deferred window position structure.</span></span></p>
<p><span data-ttu-id="37b6c-392">Esse tipo é declarado em WinUser. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-392">This type is declared in WinUser.h as follows:</span></span></p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-394">Um identificador para um <a href="/windows/desktop/gdi/metafiles">metarquivo avançado</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-394">A handle to an <a href="/windows/desktop/gdi/metafiles">enhanced metafile</a>.</span></span></p>
<p><span data-ttu-id="37b6c-395">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-395">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-397">Um identificador para um arquivo aberto pelo <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, não <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-397">A handle to a file opened by <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, not <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-398">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-398">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-400">Um identificador para uma <a href="/windows/desktop/gdi/about-fonts">fonte</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-400">A handle to a <a href="/windows/desktop/gdi/about-fonts">font</a>.</span></span></p>
<p><span data-ttu-id="37b6c-401">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-401">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-403">Um identificador para um objeto GDI.</span><span class="sxs-lookup"><span data-stu-id="37b6c-403">A handle to a GDI object.</span></span></p>
<p><span data-ttu-id="37b6c-404">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-404">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-406">Um identificador para um bloco de memória global.</span><span class="sxs-lookup"><span data-stu-id="37b6c-406">A handle to a global memory block.</span></span></p>
<p><span data-ttu-id="37b6c-407">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-407">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-409">Um identificador para um <a href="/windows/desktop/winmsg/hooks">gancho</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-409">A handle to a <a href="/windows/desktop/winmsg/hooks">hook</a>.</span></span></p>
<p><span data-ttu-id="37b6c-410">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-410">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-412">Um identificador para um <a href="/windows/desktop/menurc/icons">ícone</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-412">A handle to an <a href="/windows/desktop/menurc/icons">icon</a>.</span></span></p>
<p><span data-ttu-id="37b6c-413">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-413">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-415">Um identificador para uma instância.</span><span class="sxs-lookup"><span data-stu-id="37b6c-415">A handle to an instance.</span></span> <span data-ttu-id="37b6c-416">Esse é o endereço base do módulo na memória.</span><span class="sxs-lookup"><span data-stu-id="37b6c-416">This is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="37b6c-417"><strong>HMODULE</strong> e <strong>HINSTANCE</strong> são os mesmos hoje, mas representaram coisas diferentes no Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-417"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same today, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="37b6c-418">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-418">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-420">Um identificador para uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-420">A handle to a registry key.</span></span></p>
<p><span data-ttu-id="37b6c-421">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-421">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-423">Um identificador de localidade de entrada.</span><span class="sxs-lookup"><span data-stu-id="37b6c-423">An input locale identifier.</span></span></p>
<p><span data-ttu-id="37b6c-424">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-424">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-426">Um identificador para um bloco de memória local.</span><span class="sxs-lookup"><span data-stu-id="37b6c-426">A handle to a local memory block.</span></span></p>
<p><span data-ttu-id="37b6c-427">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-427">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-429">Um identificador para um <a href="/windows/desktop/menurc/menus">menu</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-429">A handle to a <a href="/windows/desktop/menurc/menus">menu</a>.</span></span></p>
<p><span data-ttu-id="37b6c-430">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-430">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-432">Um identificador para um <a href="/windows/desktop/gdi/metafiles">metarquivo</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-432">A handle to a <a href="/windows/desktop/gdi/metafiles">metafile</a>.</span></span></p>
<p><span data-ttu-id="37b6c-433">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-433">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-435">Um identificador para um módulo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-435">A handle to a module.</span></span> <span data-ttu-id="37b6c-436">O é o endereço base do módulo na memória.</span><span class="sxs-lookup"><span data-stu-id="37b6c-436">The is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="37b6c-437"><strong>HMODULE</strong> e <strong>HINSTANCE</strong> são os mesmos nas versões atuais do Windows, mas representaram coisas diferentes no Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-437"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same in current versions of Windows, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="37b6c-438">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-438">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-440">Um identificador para um monitor de exibição.</span><span class="sxs-lookup"><span data-stu-id="37b6c-440">A handle to a display monitor.</span></span></p>
<p><span data-ttu-id="37b6c-441">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-441">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-443">Um identificador para uma paleta.</span><span class="sxs-lookup"><span data-stu-id="37b6c-443">A handle to a palette.</span></span></p>
<p><span data-ttu-id="37b6c-444">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-444">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-446">Um identificador para uma <a href="/windows/desktop/gdi/pens">caneta</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-446">A handle to a <a href="/windows/desktop/gdi/pens">pen</a>.</span></span></p>
<p><span data-ttu-id="37b6c-447">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-447">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-448"><span id="HRESULT"></span><span id="hresult"></span><strong>RESULTADO</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-449">Os códigos de retorno usados pelas interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="37b6c-449">The return codes used by COM interfaces.</span></span> <span data-ttu-id="37b6c-450">Para obter mais informações, consulte <a href="/windows/desktop/com/structure-of-com-error-codes">estrutura dos códigos de erro com</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-450">For more information, see <a href="/windows/desktop/com/structure-of-com-error-codes">Structure of the COM Error Codes</a>.</span></span> <span data-ttu-id="37b6c-451">Para testar um valor <strong>HRESULT</strong> , use as macros <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>com falha e com</strong></a> <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>êxito</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="37b6c-451">To test an <strong>HRESULT</strong> value, use the <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> and <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> macros.</span></span></p>
<p><span data-ttu-id="37b6c-452">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-452">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-454">Um identificador para uma <a href="/windows/desktop/gdi/regions">região</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-454">A handle to a <a href="/windows/desktop/gdi/regions">region</a>.</span></span></p>
<p><span data-ttu-id="37b6c-455">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-455">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-457">Um identificador para um recurso.</span><span class="sxs-lookup"><span data-stu-id="37b6c-457">A handle to a resource.</span></span></p>
<p><span data-ttu-id="37b6c-458">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-458">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-460">Um identificador para uma cadeia de caracteres DDE.</span><span class="sxs-lookup"><span data-stu-id="37b6c-460">A handle to a DDE string.</span></span></p>
<p><span data-ttu-id="37b6c-461">Esse tipo é declarado em ddeml. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-461">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-463">Um identificador para uma <a href="/windows/desktop/winstation/window-stations">estação de janela</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-463">A handle to a <a href="/windows/desktop/winstation/window-stations">window station</a>.</span></span></p>
<p><span data-ttu-id="37b6c-464">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-464">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-466">Um identificador para uma <a href="/windows/desktop/winmsg/windows">janela</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-466">A handle to a <a href="/windows/desktop/winmsg/windows">window</a>.</span></span></p>
<p><span data-ttu-id="37b6c-467">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-467">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-468"><span id="INT"></span><span id="int"></span><strong>INTEIRO</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-469">Um inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-469">A 32-bit signed integer.</span></span> <span data-ttu-id="37b6c-470">O intervalo é de-2147483648 a 2147483647 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-470">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-471">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-471">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-473">Um tipo de inteiro assinado para precisão de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-473">A signed integer type for pointer precision.</span></span> <span data-ttu-id="37b6c-474">Use ao converter um ponteiro para um inteiro para executar aritmética de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-474">Use when casting a pointer to an integer to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="37b6c-475">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-475">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-476">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-476">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-478">Um inteiro com sinal de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-478">An 8-bit signed integer.</span></span></p>
<p><span data-ttu-id="37b6c-479">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-479">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-481">Um inteiro de 16 bits com sinal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-481">A 16-bit signed integer.</span></span></p>
<p><span data-ttu-id="37b6c-482">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-482">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-484">Um inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-484">A 32-bit signed integer.</span></span> <span data-ttu-id="37b6c-485">O intervalo é de-2147483648 a 2147483647 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-485">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-486">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-486">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-488">Um inteiro com sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-488">A 64-bit signed integer.</span></span> <span data-ttu-id="37b6c-489">O intervalo é-9.223.372.036.854.775.808 até 9223372036854775807 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-489">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-490">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-490">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-492">Um identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="37b6c-492">A language identifier.</span></span> <span data-ttu-id="37b6c-493">Para obter mais informações, consulte <a href="/windows/desktop/Intl/language-identifiers">identificadores de idioma</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-493">For more information, see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>.</span></span></p>
<p><span data-ttu-id="37b6c-494">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-494">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-496">Um identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="37b6c-496">A locale identifier.</span></span> <span data-ttu-id="37b6c-497">Para obter mais informações, consulte <a href="/windows/desktop/Intl/locale-identifiers">identificadores de localidade</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-497">For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.</span></span></p>
<p><span data-ttu-id="37b6c-498">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-498">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-500">Um tipo de informação de localidade.</span><span class="sxs-lookup"><span data-stu-id="37b6c-500">A locale information type.</span></span> <span data-ttu-id="37b6c-501">Para obter uma lista, consulte <a href="/windows/desktop/Intl/locale-information-constants">constantes de informações de localidade</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-501">For a list, see <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>.</span></span></p>
<p><span data-ttu-id="37b6c-502">Esse tipo é declarado em WinNls. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-502">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-504">Um identificador de grupo de idiomas.</span><span class="sxs-lookup"><span data-stu-id="37b6c-504">A language group identifier.</span></span> <span data-ttu-id="37b6c-505">Para obter uma lista, consulte <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-505">For a list, see <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-506">Esse tipo é declarado em WinNls. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-506">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-507"><span id="LONG"></span><span id="long"></span><strong>Longas</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-507"><span id="LONG"></span><span id="long"></span><strong>LONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-508">Um inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-508">A 32-bit signed integer.</span></span> <span data-ttu-id="37b6c-509">O intervalo é de-2147483648 a 2147483647 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-509">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-510">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-510">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-512">Um inteiro com sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-512">A 64-bit signed integer.</span></span> <span data-ttu-id="37b6c-513">O intervalo é-9.223.372.036.854.775.808 até 9223372036854775807 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-513">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-514">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-514">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-515">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-515">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-517">Um tipo longo assinado para a precisão do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-517">A signed long type for pointer precision.</span></span> <span data-ttu-id="37b6c-518">Use ao converter um ponteiro para um longo para executar a aritmética do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-518">Use when casting a pointer to a long to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="37b6c-519">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-519">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-520">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-520">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-522">Um inteiro com sinal de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-522">A 32-bit signed integer.</span></span> <span data-ttu-id="37b6c-523">O intervalo é de-2147483648 a 2147483647 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-523">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-524">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-524">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-526">Um inteiro com sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-526">A 64-bit signed integer.</span></span> <span data-ttu-id="37b6c-527">O intervalo é-9.223.372.036.854.775.808 até 9223372036854775807 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-527">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-528">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-528">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-530">Um parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="37b6c-530">A message parameter.</span></span></p>
<p><span data-ttu-id="37b6c-531">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-531">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-533">Um ponteiro para um <a href="#bool"><strong>bool</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-533">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-534">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-534">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-536">Um ponteiro para um <a href="#byte"><strong>byte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-536">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-537">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-537">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-539">Um ponteiro para um valor de <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="37b6c-539">A pointer to a <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> value.</span></span></p>
<p><span data-ttu-id="37b6c-540">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-540">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-542">Um ponteiro para uma cadeia de caracteres constante terminada em nulo de caracteres ANSI (Windows de 8 bits).</span><span class="sxs-lookup"><span data-stu-id="37b6c-542">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="37b6c-543">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-543">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-544">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-544">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-546">Um <a href="#lpcwstr"><strong>LPCWSTR</strong></a> se <strong>Unicode</strong> estiver definido; caso contrário, <a href="#lpcstr"><strong>LPCSTR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="37b6c-546">An <a href="#lpcwstr"><strong>LPCWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpcstr"><strong>LPCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="37b6c-547">Para obter mais informações, consulte <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de dados do Windows para cadeias de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-547">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="37b6c-548">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-548">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-549">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-549">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-551">Um ponteiro para uma constante de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-551">A pointer to a constant of any type.</span></span></p>
<p><span data-ttu-id="37b6c-552">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-552">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-554">Um ponteiro para uma cadeia de caracteres constante terminada em nulo de caracteres Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-554">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="37b6c-555">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-555">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-556">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-556">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-558">Um ponteiro para um <a href="#dword"><strong>DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-558">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-559">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-559">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-561">Um ponteiro para um <a href="#handle"><strong>identificador</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-561">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-562">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-562">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-564">Um ponteiro para um <a href="#int"><strong>int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-564">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-565">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-565">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-567">Um ponteiro para um <a href="#long"><strong>longo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-567">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-568">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-568">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-570">Um ponteiro para uma cadeia de caracteres do Windows de 8 bits terminada por nulo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-570">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="37b6c-571">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-571">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-572">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-572">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-574">Um <a href="#lpwstr"><strong>LPWSTR</strong></a> se o <strong>Unicode</strong> for definido, um <a href="#lpstr"><strong>LPSTR</strong></a> , caso contrário.</span><span class="sxs-lookup"><span data-stu-id="37b6c-574">An <a href="#lpwstr"><strong>LPWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpstr"><strong>LPSTR</strong></a> otherwise.</span></span> <span data-ttu-id="37b6c-575">Para obter mais informações, consulte <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de dados do Windows para cadeias de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-575">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="37b6c-576">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-576">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-577">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-577">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-579">Um ponteiro para qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-579">A pointer to any type.</span></span></p>
<p><span data-ttu-id="37b6c-580">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-580">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-582">Um ponteiro para uma <a href="#word"><strong>palavra</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-582">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-583">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-583">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-585">Um ponteiro para uma cadeia de caracteres Unicode de 16 bits terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-585">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="37b6c-586">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-586">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-587">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-587">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-589">Resultado assinado do processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="37b6c-589">Signed result of message processing.</span></span></p>
<p><span data-ttu-id="37b6c-590">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-590">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-592">Um ponteiro para um <a href="#bool"><strong>bool</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-592">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-593">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-593">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-595">Um ponteiro para um <a href="#boolean"><strong>booliano</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-595">A pointer to a <a href="#boolean"><strong>BOOLEAN</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-596">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-596">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-598">Um ponteiro para um <a href="#byte"><strong>byte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-598">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-599">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-599">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-601">Um ponteiro para um <a href="#char"><strong>Char</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-601">A pointer to a <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-602">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-602">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-604">Um ponteiro para uma cadeia de caracteres constante terminada em nulo de caracteres ANSI (Windows de 8 bits).</span><span class="sxs-lookup"><span data-stu-id="37b6c-604">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="37b6c-605">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-605">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-606">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-606">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-608">Um <a href="#pcwstr"><strong>PCWSTR</strong></a> se o <strong>Unicode</strong> estiver definido; caso contrário, <a href="#pcstr"><strong>PCSTR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="37b6c-608">A <a href="#pcwstr"><strong>PCWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pcstr"><strong>PCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="37b6c-609">Para obter mais informações, consulte <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de dados do Windows para cadeias de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-609">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="37b6c-610">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-610">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-611">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-611">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-613">Um ponteiro para uma cadeia de caracteres constante terminada em nulo de caracteres Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-613">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="37b6c-614">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-614">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-615">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-615">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-617">Um ponteiro para um <a href="#dword"><strong>DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-617">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-618">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-618">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-620">Um ponteiro para um <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-620">A pointer to a <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-621">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-621">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-623">Um ponteiro para um <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-623">A pointer to a <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-624">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-624">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-626">Um ponteiro para um <a href="#dword32"><strong>DWORD32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-626">A pointer to a <a href="#dword32"><strong>DWORD32</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-627">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-627">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-629">Um ponteiro para um <a href="#dword64"><strong>DWORD64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-629">A pointer to a <a href="#dword64"><strong>DWORD64</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-630">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-630">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-632">Um ponteiro para um <a href="#float"><strong>float</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-632">A pointer to a <a href="#float"><strong>FLOAT</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-633">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-633">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-635">Um ponteiro para um <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-635">A pointer to a <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-636">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-636">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-637">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-637">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-639">Um ponteiro para um <a href="#handle"><strong>identificador</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-639">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-640">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-640">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-642">Um ponteiro para um <a href="#hkey"><strong>HKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-642">A pointer to an <a href="#hkey"><strong>HKEY</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-643">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-643">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-644"><span id="PINT"></span><span id="pint"></span><strong>APONTE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-644"><span id="PINT"></span><span id="pint"></span><strong>PINT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-645">Um ponteiro para um <a href="#int"><strong>int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-645">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-646">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-646">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-648">Um ponteiro para um <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-648">A pointer to an <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-649">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-649">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-651">Um ponteiro para um <a href="#int8"><strong>INT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-651">A pointer to an <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-652">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-652">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-654">Um ponteiro para um <a href="#int16"><strong>Int16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-654">A pointer to an <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-655">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-655">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-657">Um ponteiro para um <a href="#int32"><strong>INT32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-657">A pointer to an <a href="#int32"><strong>INT32</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-658">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-658">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-660">Um ponteiro para um <a href="#int64"><strong>Int64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-660">A pointer to an <a href="#int64"><strong>INT64</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-661">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-661">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-663">Um ponteiro para um <a href="#lcid"><strong>LCID</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-663">A pointer to an <a href="#lcid"><strong>LCID</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-664">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-664">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-666">Um ponteiro para um <a href="#long"><strong>longo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-666">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-667">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-667">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-669">Um ponteiro para um <a href="#longlong"><strong>LONGLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-669">A pointer to a <a href="#longlong"><strong>LONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-670">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-670">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-672">Um ponteiro para um <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-672">A pointer to a <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-673">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-673">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-675">Um ponteiro para um <a href="#long32"><strong>LONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-675">A pointer to a <a href="#long32"><strong>LONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-676">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-676">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-678">Um ponteiro para um <a href="#long64"><strong>LONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-678">A pointer to a <a href="#long64"><strong>LONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-679">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-679">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-681">Um ponteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-681">A 32-bit pointer.</span></span> <span data-ttu-id="37b6c-682">Em um sistema de 32 bits, esse é um ponteiro nativo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-682">On a 32-bit system, this is a native pointer.</span></span> <span data-ttu-id="37b6c-683">Em um sistema de 64 bits, esse é um ponteiro de bit de 64 truncado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-683">On a 64-bit system, this is a truncated 64-bit pointer.</span></span></p>
<p><span data-ttu-id="37b6c-684">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-684">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-685">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-685">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-687">Um ponteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-687">A 64-bit pointer.</span></span> <span data-ttu-id="37b6c-688">Em um sistema de 64 bits, esse é um ponteiro nativo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-688">On a 64-bit system, this is a native pointer.</span></span> <span data-ttu-id="37b6c-689">Em um sistema de 32 bits, esse é um ponteiro de bit de 32 de sinal estendido.</span><span class="sxs-lookup"><span data-stu-id="37b6c-689">On a 32-bit system, this is a sign-extended 32-bit pointer.</span></span></p>
<p><span data-ttu-id="37b6c-690">Observe que não é seguro assumir o estado do bit de ponteiro alto.</span><span class="sxs-lookup"><span data-stu-id="37b6c-690">Note that it is not safe to assume the state of the high pointer bit.</span></span></p>
<p><span data-ttu-id="37b6c-691">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-691">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-692">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-692">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-694">Um ponteiro assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-694">A signed pointer.</span></span></p>
<p><span data-ttu-id="37b6c-695">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-695">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-697">Um ponteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-697">An unsigned pointer.</span></span></p>
<p><span data-ttu-id="37b6c-698">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-698">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-700">Um ponteiro para um <a href="#short"><strong>curto</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-700">A pointer to a <a href="#short"><strong>SHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-701">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-701">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-703">Um ponteiro para um <a href="#size_t"><strong>size_t</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-703">A pointer to a <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-704">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-704">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-706">Um ponteiro para um <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-706">A pointer to a <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-707">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-707">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-709">Um ponteiro para uma cadeia de caracteres do Windows de 8 bits terminada por nulo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-709">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="37b6c-710">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-710">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-711">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-711">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-713">Um ponteiro para um <a href="#tbyte"><strong>Tbyte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-713">A pointer to a <a href="#tbyte"><strong>TBYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-714">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-714">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-716">Um ponteiro para um <a href="#tchar"><strong>TCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-716">A pointer to a <a href="#tchar"><strong>TCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-717">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-717">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-719">Um <a href="#pwstr"><strong>PWSTR</strong></a> se o <strong>Unicode</strong> estiver definido; caso contrário, <a href="#pstr"><strong>PSTR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="37b6c-719">A <a href="#pwstr"><strong>PWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pstr"><strong>PSTR</strong></a> otherwise.</span></span> <span data-ttu-id="37b6c-720">Para obter mais informações, consulte <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de dados do Windows para cadeias de caracteres</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-720">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="37b6c-721">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-721">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-722">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-722">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-724">Um ponteiro para um <a href="#uchar"><strong>UCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-724">A pointer to a <a href="#uchar"><strong>UCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-725">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-725">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-727">Um ponteiro para um <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-727">A pointer to a <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-728">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-728">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-729">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-729">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-731">Um ponteiro para um <a href="#uint"><strong>uint</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-731">A pointer to a <a href="#uint"><strong>UINT</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-732">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-732">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-734">Um ponteiro para um <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-734">A pointer to a <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-735">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-735">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-737">Um ponteiro para um <a href="#uint8"><strong>UINT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-737">A pointer to a <a href="#uint8"><strong>UINT8</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-738">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-738">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-740">Um ponteiro para um <a href="#uint16"><strong>UINT16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-740">A pointer to a <a href="#uint16"><strong>UINT16</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-741">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-741">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-743">Um ponteiro para um <a href="#uint32"><strong>UINT32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-743">A pointer to a <a href="#uint32"><strong>UINT32</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-744">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-744">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-746">Um ponteiro para um <a href="#uint64"><strong>UINT64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-746">A pointer to a <a href="#uint64"><strong>UINT64</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-747">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-747">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-749">Um ponteiro para um <a href="#ulong"><strong>ULONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-749">A pointer to a <a href="#ulong"><strong>ULONG</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-750">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-750">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-752">Um ponteiro para um <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-752">A pointer to a <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-753">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-753">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-755">Um ponteiro para um <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-755">A pointer to a <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-756">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-756">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-758">Um ponteiro para um <a href="#ulong32"><strong>ULONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-758">A pointer to a <a href="#ulong32"><strong>ULONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-759">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-759">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-761">Um ponteiro para um <a href="#ulong64"><strong>ULONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-761">A pointer to a <a href="#ulong64"><strong>ULONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-762">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-762">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-764">Um ponteiro para um <a href="#ushort"><strong>UShort</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-764">A pointer to a <a href="#ushort"><strong>USHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-765">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-765">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-767">Um ponteiro para qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-767">A pointer to any type.</span></span></p>
<p><span data-ttu-id="37b6c-768">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-768">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-770">Um ponteiro para um <a href="#wchar"><strong>WCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-770">A pointer to a <a href="#wchar"><strong>WCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-771">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-771">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-773">Um ponteiro para uma <a href="#word"><strong>palavra</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-773">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-774">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-774">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-776">Um ponteiro para uma cadeia de caracteres Unicode de 16 bits terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-776">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="37b6c-777">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-777">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-778">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-778">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-780">Um inteiro sem sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-780">A 64-bit unsigned integer.</span></span></p>
<p><span data-ttu-id="37b6c-781">Esse tipo é declarado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-781">This type is declared as follows:</span></span></p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-783">Um identificador para um banco de dados do Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="37b6c-783">A handle to a service control manager database.</span></span> <span data-ttu-id="37b6c-784">Para obter mais informações, consulte <a href="/windows/desktop/Services/scm-handles">identificadores SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-784">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="37b6c-785">Esse tipo é declarado em WinSvc. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-785">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-787">Um bloqueio para um banco de dados do Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="37b6c-787">A lock to a service control manager database.</span></span> <span data-ttu-id="37b6c-788">Para obter mais informações, consulte <a href="/windows/desktop/Services/scm-handles">identificadores SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-788">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="37b6c-789">Esse tipo é declarado em WinSvc. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-789">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-791">Um identificador para um valor de status de serviço.</span><span class="sxs-lookup"><span data-stu-id="37b6c-791">A handle to a service status value.</span></span> <span data-ttu-id="37b6c-792">Para obter mais informações, consulte <a href="/windows/desktop/Services/scm-handles">identificadores SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-792">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="37b6c-793">Esse tipo é declarado em WinSvc. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-793">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-794"><span id="SHORT"></span><span id="short"></span><strong>BAIXO</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-794"><span id="SHORT"></span><span id="short"></span><strong>SHORT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-795">Um inteiro de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-795">A 16-bit integer.</span></span> <span data-ttu-id="37b6c-796">O intervalo é de-32768 a 32767 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-796">The range is -32768 through 32767 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-797">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-797">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-799">O número máximo de bytes aos quais um ponteiro pode apontar.</span><span class="sxs-lookup"><span data-stu-id="37b6c-799">The maximum number of bytes to which a pointer can point.</span></span> <span data-ttu-id="37b6c-800">Use para uma contagem que deve abranger o intervalo completo de um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="37b6c-800">Use for a count that must span the full range of a pointer.</span></span></p>
<p><span data-ttu-id="37b6c-801">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-801">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-803">Uma versão assinada do <a href="#size_t"><strong>size_t</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-803">A signed version of <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-804">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-804">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-806">Um <a href="#char"><strong>caractere</strong></a> <a href="#wchar"><strong>WCHAR</strong></a> se <strong>Unicode</strong> estiver definido, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="37b6c-806">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="37b6c-807">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-807">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-808">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-808">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-810">Um <a href="#char"><strong>caractere</strong></a> <a href="#wchar"><strong>WCHAR</strong></a> se <strong>Unicode</strong> estiver definido, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="37b6c-810">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="37b6c-811">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-811">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-812">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-812">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-814">Um <a href="#char"><strong>Char</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-814">An unsigned <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-815">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-815">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-817">Um <a href="#half_ptr"><strong>HALF_PTR</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-817">An unsigned <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span> <span data-ttu-id="37b6c-818">Use em uma estrutura que contém um ponteiro e dois campos pequenos.</span><span class="sxs-lookup"><span data-stu-id="37b6c-818">Use within a structure that contains a pointer and two small fields.</span></span></p>
<p><span data-ttu-id="37b6c-819">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-819">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-820">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-820">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-822">Um <a href="#int"><strong>int</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-822">An unsigned <a href="#int"><strong>INT</strong></a>.</span></span> <span data-ttu-id="37b6c-823">O intervalo é de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-823">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-824">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-824">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-826">Um <a href="#int_ptr"><strong>INT_PTR</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-826">An unsigned <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-827">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-827">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-828">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-828">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-830">Um <a href="#int8"><strong>INT8</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-830">An unsigned <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-831">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-831">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-833">Um <a href="#int16"><strong>Int16</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-833">An unsigned <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-834">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-834">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-836">Um <a href="#int32"><strong>INT32</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-836">An unsigned <a href="#int32"><strong>INT32</strong></a>.</span></span> <span data-ttu-id="37b6c-837">O intervalo é de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-837">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-838">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-838">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-840">Um <a href="#int64"><strong>Int64</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-840">An unsigned <a href="#int64"><strong>INT64</strong></a>.</span></span> <span data-ttu-id="37b6c-841">O intervalo é de 0 a 18446744073709551615 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-841">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-842">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-842">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-844">Um <a href="#long"><strong>longo</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-844">An unsigned <a href="#long"><strong>LONG</strong></a>.</span></span> <span data-ttu-id="37b6c-845">O intervalo é de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-845">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-846">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-846">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-848">Um inteiro sem sinal de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-848">A 64-bit unsigned integer.</span></span> <span data-ttu-id="37b6c-849">O intervalo é de 0 a 18446744073709551615 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-849">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-850">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-850">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-851">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-851">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-853">Um <a href="#long_ptr"><strong>LONG_PTR</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-853">An unsigned <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="37b6c-854">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-854">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-855">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-855">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-857">Um <a href="#long32"><strong>LONG32</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-857">An unsigned <a href="#long32"><strong>LONG32</strong></a>.</span></span> <span data-ttu-id="37b6c-858">O intervalo é de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-858">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-859">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-859">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-861">Um <a href="#long64"><strong>LONG64</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-861">An unsigned <a href="#long64"><strong>LONG64</strong></a>.</span></span> <span data-ttu-id="37b6c-862">O intervalo é de 0 a 18446744073709551615 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-862">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-863">Esse tipo é declarado em BaseTsd. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-863">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-865">Uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="37b6c-865">A Unicode string.</span></span></p>
<p><span data-ttu-id="37b6c-866">Esse tipo é declarado em Winternl. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-866">This type is declared in Winternl.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37b6c-867">C++</span><span class="sxs-lookup"><span data-stu-id="37b6c-867">C++</span></span></th>
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
<td><span data-ttu-id="37b6c-868"><span id="USHORT"></span><span id="ushort"></span><strong>NUM</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-869">Um <a href="#short"><strong>curto</strong></a>não assinado.</span><span class="sxs-lookup"><span data-stu-id="37b6c-869">An unsigned <a href="#short"><strong>SHORT</strong></a>.</span></span> <span data-ttu-id="37b6c-870">O intervalo é de 0 a 65535 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-870">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-871">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-871">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-872"><span id="USN"></span><span id="usn"></span><strong>SEQÜÊNCIA</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-873">Um USN (número de sequência de atualização).</span><span class="sxs-lookup"><span data-stu-id="37b6c-873">An update sequence number (USN).</span></span></p>
<p><span data-ttu-id="37b6c-874">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-874">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-875"><span id="VOID"></span><span id="void"></span><strong>LIVRE</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-875"><span id="VOID"></span><span id="void"></span><strong>VOID</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-876">Qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="37b6c-876">Any type.</span></span></p>
<p><span data-ttu-id="37b6c-877">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-877">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-879">Um caractere Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-879">A 16-bit Unicode character.</span></span> <span data-ttu-id="37b6c-880">Para obter mais informações, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">conjuntos de caracteres usados por fontes</a>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-880">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="37b6c-881">Esse tipo é declarado em WinNT. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-881">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-882"><span id="WINAPI"></span><span id="winapi"></span><strong>Winapi tenha</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-883">A Convenção de chamada para funções do sistema.</span><span class="sxs-lookup"><span data-stu-id="37b6c-883">The calling convention for system functions.</span></span></p>
<p><span data-ttu-id="37b6c-884">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-884">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>#define WINAPI __stdcall</code></p>
<p><span data-ttu-id="37b6c-885"><strong>Retorno de chamada</strong>, <strong>Winapi tenha</strong>e <strong>APIENTRY</strong> são usados para definir funções com a Convenção de chamada __stdcall.</span><span class="sxs-lookup"><span data-stu-id="37b6c-885"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="37b6c-886">A maioria das funções na API do Windows é declarada usando <strong>Winapi tenha</strong>.</span><span class="sxs-lookup"><span data-stu-id="37b6c-886">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="37b6c-887">Talvez você queira usar o <strong>retorno de chamada</strong> para as funções de retorno de chamada implementadas para ajudar a identificar a função como uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="37b6c-887">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37b6c-888"><span id="WORD"></span><span id="word"></span><strong>TEXTOS</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-888"><span id="WORD"></span><span id="word"></span><strong>WORD</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-889">Um inteiro sem sinal de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="37b6c-889">A 16-bit unsigned integer.</span></span> <span data-ttu-id="37b6c-890">O intervalo é de 0 a 65535 decimal.</span><span class="sxs-lookup"><span data-stu-id="37b6c-890">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="37b6c-891">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-891">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37b6c-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="37b6c-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span></span></td>
<td><p><span data-ttu-id="37b6c-893">Um parâmetro de mensagem.</span><span class="sxs-lookup"><span data-stu-id="37b6c-893">A message parameter.</span></span></p>
<p><span data-ttu-id="37b6c-894">Esse tipo é declarado em WinDef. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37b6c-894">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="37b6c-895">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37b6c-895">Requirements</span></span>



| <span data-ttu-id="37b6c-896">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b6c-896">Requirement</span></span> | <span data-ttu-id="37b6c-897">Valor</span><span class="sxs-lookup"><span data-stu-id="37b6c-897">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37b6c-898">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37b6c-898">Minimum supported client</span></span><br/> | <span data-ttu-id="37b6c-899">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="37b6c-899">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="37b6c-900">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37b6c-900">Minimum supported server</span></span><br/> | <span data-ttu-id="37b6c-901">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37b6c-901">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                |
| <span data-ttu-id="37b6c-902">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37b6c-902">Header</span></span><br/>                   | <dl> <span data-ttu-id="37b6c-903"><dt>BaseTsd. h; </dt> <dt>WinDef. h; </dt> <dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b6c-903"><dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt></span></span> </dl> |
