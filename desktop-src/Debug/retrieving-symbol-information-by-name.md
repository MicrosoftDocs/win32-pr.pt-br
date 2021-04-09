---
description: O código a seguir demonstra como chamar a função SymFromName.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Recuperando informações de símbolo por nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f5f4477be4f494383c7d9c1ca462f3beb69690
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089081"
---
# <a name="retrieving-symbol-information-by-name"></a>Recuperando informações de símbolo por nome

O código a seguir demonstra como chamar a função [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Essa função preenche uma estrutura [**de \_ informações de símbolo**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Como o nome é variável em comprimento, você deve fornecer um buffer que seja grande o suficiente para manter o nome armazenado no final da estrutura **de \_ informações de símbolo** . Além disso, o membro **MaxNameLen** deve ser definido como o número de bytes reservados para o nome. Neste exemplo, szSymbolName é um buffer que armazena o nome do símbolo solicitado. O exemplo supõe que você tenha inicializado o manipulador de símbolo usando o código na [inicialização do manipulador de símbolo](initializing-the-symbol-handler.md).


```C++
TCHAR szSymbolName[MAX_SYM_NAME];
ULONG64 buffer[(sizeof(SYMBOL_INFO) +
    MAX_SYM_NAME * sizeof(TCHAR) +
    sizeof(ULONG64) - 1) /
    sizeof(ULONG64)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

_tcscpy_s(szSymbolName, MAX_SYM_NAME, TEXT("WinMain"));
pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromName(hProcess, szSymbolName, pSymbol))
{
    // SymFromName returned success
}
else
{
    // SymFromName failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymFromName returned error : %d\n"), error);
}
```



Se um aplicativo tiver um módulo ou nome de arquivo de origem, bem como informações de número de linha, ele poderá usar [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) para recuperar um endereço de código virtual. Essa função requer um ponteiro para uma [**estrutura \_ LINE64 do imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para receber o endereço de código virtual. Observe que o manipulador de símbolos pode recuperar informações de número de linha somente quando \_ \_ a opção SYMOPT carregar linhas é definida usando a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Essa opção deve ser definida antes de carregar o módulo. O parâmetro szModuleName contém o nome do módulo de origem; é opcional e pode ser **NULL**. O parâmetro szFileName deve conter o nome do arquivo de origem e o parâmetro dwLineNumber deve conter o número de linha para o qual o endereço virtual será recuperado.


```C++
TCHAR  szModuleName[MAX_PATH];
TCHAR  szFileName[MAX_PATH];
DWORD  dwLineNumber;
LONG   lDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
_tcscpy_s(szModuleName, MAX_PATH, TEXT("MyApp"));
_tcscpy_s(szFileName, MAX_PATH, TEXT("main.c"));
dwLineNumber = 248;

if (SymGetLineFromName64(hProcess, szModuleName, szFileName,
    dwLineNumber, &lDisplacement, &line))
{
    // SymGetLineFromName64 returned success
}
else
{
    // SymGetLineFromName64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromName64 returned error : %d\n"), error);
}
```



 

 



