---
title: Usando os cabeçalhos do Windows
description: Use os arquivos de cabeçalho do Windows para criar aplicativos que usam a API do Windows.
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- API do Windows, arquivos de cabeçalho
- C2065
- WINVER
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 4d27b14a6e545db9a9a38c205012b149942adf7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366515"
---
# <a name="using-the-windows-headers"></a>Usando os cabeçalhos do Windows

Os arquivos de cabeçalho para a API do Windows permitem criar aplicativos de 32 e 64 bits. Eles incluem declarações para as versões Unicode e ANSI da API. Para obter mais informações, consulte [Unicode na API do Windows](/windows/desktop/Intl/unicode-in-the-windows-api). Eles usam [tipos de dados](windows-data-types.md) que permitem que você crie versões de 32 e 64 bits de seu aplicativo a partir de uma base de código de origem única. Para obter mais informações, consulte [preparando-se para o Windows de 64 bits](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows). Recursos adicionais incluem [anotações de cabeçalho](header-annotations.md) e [verificação de tipo estrito](strict-type-checking.md).

-   [Visual C++ e os arquivos de cabeçalho do Windows](#visual-c-and-the-windows-header-files)
-   [Macros para declarações condicionais](#macros-for-conditional-declarations)
-   [Definindo WINVER ou \_ Win32 \_ Winnt](#setting-winver-or-_win32_winnt)
-   [Controlando a embalagem da estrutura](#controlling-structure-packing)
-   [Compilações mais rápidas com arquivos de cabeçalho menores](#faster-builds-with-smaller-header-files)
-   [Tópicos relacionados](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ e os arquivos de cabeçalho do Windows

Microsoft Visual C++ inclui cópias dos arquivos de cabeçalho do Windows que foram atuais no momento em que Visual C++ foi lançado. Portanto, se você instalar arquivos de cabeçalho atualizados de um SDK, poderá acabar com várias versões dos arquivos de cabeçalho do Windows em seu computador. Se você não tiver certeza de que está usando a versão mais recente dos arquivos de cabeçalho do SDK, receberá o seguinte código de erro ao compilar o código que usa recursos que foram introduzidos depois que Visual C++ foi lançado: erro C2065: identificador não declarado.

## <a name="macros-for-conditional-declarations"></a>Macros para declarações condicionais

Determinadas funções que dependem de uma versão específica do Windows são declaradas usando código condicional. Isso permite que você use o compilador para detectar se seu aplicativo usa funções que não têm suporte em suas versões de destino do Windows. Para compilar um aplicativo que usa essas funções, você deve definir as macros apropriadas. Caso contrário, você receberá a mensagem de erro C2065.

Os arquivos de cabeçalho do Windows usam macros para indicar quais versões do Windows oferecem suporte a muitos elementos de programação. Portanto, você deve definir essas macros para usar a nova funcionalidade introduzida em cada versão principal do sistema operacional. (Os arquivos de cabeçalho individuais podem usar macros diferentes; portanto, se ocorrerem problemas de compilação, verifique o arquivo de cabeçalho que contém a definição para definições condicionais.) Para obter mais informações, consulte SdkDdkVer. h.

A tabela a seguir descreve as macros preferenciais usadas nos arquivos de cabeçalho do Windows. Se você definir a \_ versão NTDDI, também deverá definir o \_ Win32 \_ Winnt.



| Mínimo exigido pelo sistema                       | Valor para a \_ versão NTDDI            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 "19H1"                        | **NTDDI \_ WIN10 \_ 19H1** (0x0A000007) |
| Windows 10 1809 "Redstone 5"                  | **NTDDI \_ WIN10 \_ RS5** (0x0A000006)  |
| Windows 10 1803 "Redstone 4"                  | **NTDDI \_ WIN10 \_ RS4** (0x0A000005)  |
| Windows 10 1709 "Redstone 3"                  | **NTDDI \_ WIN10 \_ RS3** (0x0A000004)  |
| Windows 10 1703 "Redstone 2"                  | **NTDDI \_ WIN10 \_ RS2** (0x0A000003)  |
| Windows 10 1607 "Redstone 1"                  | **NTDDI \_ WIN10 \_ RS1** (0x0A000002)  |
| Windows 10 1511 "limite 2"                 | **NTDDI \_ WIN10 \_ Th2** (0x0A000001)  |
| "Limite" do Windows 10 1507                   | **NTDDI \_ WIN10** (0x0A000000)       |
| Windows 8.1                                   | **NTDDI \_ WINBLUE** (0x06030000)     |
| Windows 8                                     | **NTDDI \_ WIN8** (0x06020000)        |
| Windows 7                                     | **NTDDI \_ WIN7** (0x06010000)        |
| Windows Server 2008                           | **NTDDI \_ WS08** (0x06000100)        |
| Windows Vista com Service Pack 1 (SP1)       | **NTDDI \_ VISTASP1** (0x06000100)    |
| Windows Vista                                 | **NTDDI \_ VISTA** (0x06000000)       |
| Windows Server 2003 com Service Pack 2 (SP2) | **NTDDI \_ WS03SP2** (0x05020200)     |
| Windows Server 2003 com Service Pack 1 (SP1) | **NTDDI \_ WS03SP1** (0x05020100)     |
| Windows Server 2003                           | **NTDDI \_ WS03** (0x05020000)        |
| Windows XP com Service Pack 3 (SP3)          | **NTDDI \_ WINXPSP3** (0x05010300)    |
| Windows XP com Service Pack 2 (SP2)          | **NTDDI \_ WINXPSP2** (0x05010200)    |
| Windows XP com Service Pack 1 (SP1)          | **NTDDI \_ WINXPSP1** (0x05010100)    |
| Windows XP                                    | **NTDDI \_ WINXP** (0x05010000)       |



 

As tabelas a seguir descrevem outras macros usadas nos arquivos de cabeçalho do Windows.



| Mínimo exigido pelo sistema                           | Valor mínimo para \_ Win32 \_ winnt e winver |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ Win32 \_ WinNT \_ WIN10** (0x0A00)          |
| Windows 8.1                                       | **\_ Win32 \_ WinNT \_ WINBLUE** (0x0603)        |
| Windows 8                                         | **\_ Win32 \_ WinNT \_ WIN8** (0x0602)           |
| Windows 7                                         | **\_ \_ \_ Win7 do Win32 WinNT** (0x0601)           |
| Windows Server 2008                               | **\_ Win32 \_ WinNT \_ WS08** (0x0600)           |
| Windows Vista                                     | **\_ Win32 \_ WinNT \_ Vista** (0x0600)          |
| Windows Server 2003 com SP1, Windows XP com SP2 | **\_ Win32 \_ WinNT \_ WS03** (0x0502)           |
| Windows Server 2003, Windows XP                   | **\_ Win32 \_ WinNT \_ WinXP** (0x0501)          |



 



| Versão mínima necessária          | Valor mínimo do \_ Win32 \_ IE      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11,0            | **\_ Win32 \_ IE \_ IE110** (0x0A00)   |
| Internet Explorer 10,0            | **\_ Win32 \_ IE \_ IE100** (0x0A00)   |
| Internet Explorer 9,0             | **\_ Win32 \_ IE \_ IE90** (0x0900)    |
| Internet Explorer 8.0             | **\_ Win32 \_ IE \_ IE80** (0x0800)    |
| Internet Explorer 7.0             | **\_ Win32 \_ IE \_ IE70** (0x0700)    |
| Internet Explorer 6,0 SP2         | **\_ Win32 \_ IE \_ IE60SP2** (0x0603) |
| Internet Explorer 6,0 SP1         | **\_ Win32 \_ IE \_ IE60SP1** (0x0601) |
| Internet Explorer 6,0             | **\_ Win32 \_ IE \_ IE60** (0x0600)    |
| Internet Explorer 5,5             | **\_ Win32 \_ IE \_ IE55** (0x0550)    |
| Internet Explorer 5, 1            | **\_ Win32 \_ IE \_ IE501** (0x0501)   |
| Internet Explorer 5,0, 5.0 a, 5.0 b | **\_ Win32 \_ IE \_ IE50** (0x0500)    |



 

## <a name="setting-winver-or-_win32_winnt"></a>Definindo WINVER ou \_ Win32 \_ Winnt

Você pode definir esses símbolos usando a \# instrução define em cada arquivo de origem ou especificando a opção/d do compilador com suporte pelo Visual C++.

Por exemplo, para definir WINVER em seu arquivo de origem, use a seguinte instrução:

`#define WINVER 0x0502`

Para definir \_ \_ o Win32 WinNT em seu arquivo de origem, use a seguinte instrução:

`#define _WIN32_WINNT 0x0502`

Para definir o \_ Win32 \_ WinNT usando a opção de compilador/d, use o seguinte comando:

**cl-c/d \_ WIN32 \_ WinNT = 0x0502** _Source_**. cpp**

Para obter informações sobre como usar a opção de compilador/D, consulte [/d (definições de pré-processador)](/cpp/build/reference/d-preprocessor-definitions).

Observe que alguns recursos introduzidos na versão mais recente do Windows podem ser adicionados a um service pack para uma versão anterior do Windows. Portanto, para direcionar um service pack, talvez seja necessário definir \_ \_ o Win32 WinNT com o valor da próxima versão principal do sistema operacional. Por exemplo, a função [**GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) foi introduzida no Windows Server 2003 e é condicionalmente definida se o \_ Win32 \_ WinNT for 0x0502 ou superior. Essa função também foi adicionada ao Windows XP com SP1. Portanto, se você definiu \_ o Win32 \_ WinNT como 0x0501 para o Windows XP de destino, perderia recursos que estão definidos no Windows XP com SP1.

## <a name="controlling-structure-packing"></a>Controlando a embalagem da estrutura

Os projetos devem ser compilados para usar a embalagem de estrutura padrão, que é 8 bytes no momento porque o maior tipo integral é 8 bytes. Isso garante que todos os tipos de estrutura dentro dos arquivos de cabeçalho sejam compilados no aplicativo com o mesmo alinhamento esperado pela API do Windows. Ele também garante que as estruturas com valores de 8 bytes estejam alinhadas corretamente e não causarão falhas de alinhamento em processadores que impõem o alinhamento de dados.

Para obter mais informações, consulte [/ZP (alinhamento de membro de struct)](/cpp/build/reference/zp-struct-member-alignment) ou [Pack](/cpp/preprocessor/pack).

## <a name="faster-builds-with-smaller-header-files"></a>Compilações mais rápidas com arquivos de cabeçalho menores

Você pode reduzir o tamanho dos arquivos de cabeçalho do Windows excluindo algumas das declarações de API menos comuns da seguinte maneira:

-   Defina \_ o Win32 Lean \_ e \_ a média para excluir APIs como criptografia, DDE, RPC, Shell e Windows Sockets.

    `#define WIN32_LEAN_AND_MEAN`

-   Defina um ou mais dos símbolos sem *API* para excluir a API. Por exemplo, NOCOMM exclui a API de comunicação serial. Para obter uma lista de suporte sem símbolos de *API* , consulte Windows. h.

    `#define NOCOMM`

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SDK do Windows site de download](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 