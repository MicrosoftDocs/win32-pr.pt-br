---
description: O código a seguir demonstra como chamar a função SymFromAddr.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Recuperando informações de símbolo por endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ad9d2879dbfd5820c4aa6c2e7563a1575ebe1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089082"
---
# <a name="retrieving-symbol-information-by-address"></a>Recuperando informações de símbolo por endereço

O código a seguir demonstra como chamar a função [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Essa função preenche uma estrutura [**de \_ informações de símbolo**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Como o nome é variável em comprimento, você deve fornecer um buffer que seja grande o suficiente para manter o nome armazenado no final da estrutura **de \_ informações de símbolo** . Além disso, o membro **MaxNameLen** deve ser definido como o número de bytes reservados para o nome. Neste exemplo, *dwAddress* é o endereço a ser mapeado para um símbolo. A função **SymFromAddr** irá armazenar um deslocamento no início do símbolo para o endereço em *dwDisplacement*. O exemplo supõe que você tenha inicializado o manipulador de símbolo usando o código na [inicialização do manipulador de símbolo](initializing-the-symbol-handler.md).


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



Para recuperar o número de linha de código-fonte de um endereço especificado, um aplicativo pode usar [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr). Essa função requer um ponteiro para uma [**estrutura \_ LINE64 do imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para receber o nome do arquivo de origem e o número da linha correspondente a um endereço de código especificado. Observe que o manipulador de símbolos pode recuperar informações de número de linha somente quando **SYMOPT \_ \_ linhas de carregamento** são definidas usando a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Essa opção deve ser definida antes de carregar o módulo. O parâmetro dwAddress contém o endereço de código para o qual o nome do arquivo de origem e o número da linha serão localizados.


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



