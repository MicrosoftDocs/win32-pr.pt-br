---
description: Embora DbgHelp.dll seja fornecido com todas as versões do Windows, os chamadores devem considerar o uso de uma das versões mais recentes dessa DLL, conforme encontrado no pacote de ferramentas de depuração para Windows. Para obter detalhes sobre a distribuição de DbgHelp, consulte versões do DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Chamando a biblioteca DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc06f6a0e28f163d80490647ee8f33754c249b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456882"
---
# <a name="calling-the-dbghelp-library"></a>Chamando a biblioteca DbgHelp

Embora DbgHelp.dll seja fornecido com todas as versões do Windows, os chamadores devem considerar o uso de uma das versões mais recentes dessa DLL, conforme encontrado no pacote de [ferramentas de depuração para Windows](https://www.microsoft.com/?ref=go) . Para obter detalhes sobre a distribuição de DbgHelp, consulte [versões do dbghelp](dbghelp-versions.md).

Ao usar o DbgHelp, a melhor estratégia é instalar uma cópia da biblioteca do pacote de [ferramentas de depuração para Windows](https://www.microsoft.com/?ref=go) no diretório de aplicativo logicamente adjacente ao software que o chama. Se o servidor de símbolos e o servidor de origem também forem necessários, SymSrv.dll e SrcSrv.dll deverão ser instalados no mesmo diretório que DbgHelp.dll, já que o DbgHelp chamará essas DLLs somente se compartilharem o mesmo diretório com ela. (Observe que o DbgHelp não chamará essas duas DLLs do caminho de pesquisa padrão.) Isso ajuda a evitar o uso de DLLs incompatíveis; da mesma forma, ele também melhora a segurança em geral.

O código a seguir é extraído da origem DbgHelp. Ele mostra como o DbgHelp só carrega versões do SymSrv.dll e SrcSrv.dll do mesmo diretório no qual DbgHelp.dll reside.


```C++
HINSTANCE ghinst;

// For calculating the size of arrays for safe string functions.

#ifndef cch
 #define ccht(Array, EltType) (sizeof(Array) / sizeof(EltType))
 #define cch(Array) ccht(Array, (Array)[0])
#endif

//
// LoadLibrary() a DLL, using the same directory as dbghelp.dll.
//

HMODULE 
LoadDLL(
    __in PCWSTR filename
    )
{
    WCHAR drive[10] = L"";
    WCHAR dir[MAX_PATH + 1] = L"";
    WCHAR file[MAX_PATH + 1] = L"";
    WCHAR ext[MAX_PATH + 1] = L"";
    WCHAR path[MAX_PATH + 1] = L"";
    HMODULE hm;
    
    // Chop up 'filename' into its elements.
    
    _wsplitpath_s(filename, drive, cch(drive), dir, cch(dir), file, cch(file), ext, cch(ext));

    // If 'filename' contains no path information, then get the path to our module and 
    // use it to create a fully qualified path to the module we are loading.  Then load it.
    
    if (!*drive && !*dir) 
    {
        // ghinst is the HINSTANCE of this module, initialized in DllMain or WinMain
         
        if (GetModuleFileNameW(ghinst, path, MAX_PATH)) 
        {
            _wsplitpath_s(path, drive, cch(drive), dir, cch(dir), NULL, 0, NULL, 0);
            if (*drive || *dir) 
            {
                swprintf_s(path, cch(path), L"%s%s%s%s", drive, dir, file, ext);
                hm = LoadLibrary(path);
                if (hm)
                    return hm;
            }
        }
    }
    else
    {
        // If we wanted to, we could have LoadDLL also support directories being specified
        // in 'filename'.  We could pass the path here.  The result is if no path is specified,
        // the module path is used as above, otherwise the path in 'filename' is specified.
        // But the standard search logic of LoadLibrary is still avoided.
        
        /*
        hm = LoadLibrary(path);
        if (hm)
            return hm;
        */
    }
    
    return 0;
}
```



Depois de carregar essas duas DLLs, o DbgHelp chama o [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter as funções de que precisa deles.

Normalmente, o código que chama DbgHelp.dll garante que a versão correta seja carregada instalando DbgHelp.dll no mesmo diretório que o aplicativo que iniciou o processo atual. Se o código de chamada estiver em uma DLL e não tiver acesso ou conhecimento do local do processo inicial, DbgHelp.dll deverá ser instalado junto com a DLL de chamada e o código semelhante a LoadDLL do DbgHelp deverá ser usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões do DbgHelp](dbghelp-versions.md)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
