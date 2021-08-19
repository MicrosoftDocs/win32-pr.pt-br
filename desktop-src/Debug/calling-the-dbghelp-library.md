---
description: Embora DbgHelp.dll seja fornecidas com todas as versões do Windows, os chamadores devem considerar o uso de uma das versões mais recentes dessa DLL, conforme encontrado no pacote Ferramentas de Depuração para Windows. Para obter detalhes sobre a distribuição do DbgHelp, consulte Versões do DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Chamando a biblioteca DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d6a111da8b0874a0c66fa08840e1ea4edeabf539afab2e9decf0eb19372db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957155"
---
# <a name="calling-the-dbghelp-library"></a>Chamando a biblioteca DbgHelp

Embora DbgHelp.dll seja fornecidas com todas as versões do Windows, os chamadores devem considerar o uso de uma das versões mais recentes dessa DLL, conforme encontrado no pacote Ferramentas [de Depuração](https://www.microsoft.com/?ref=go) para Windows. Para obter detalhes sobre a distribuição do DbgHelp, consulte [DbgHelp Versions](dbghelp-versions.md).

Ao usar DbgHelp, a melhor estratégia é instalar uma cópia da biblioteca do pacote Ferramentas [de Depuração](https://www.microsoft.com/?ref=go) para Windows no diretório do aplicativo logicamente adjacente ao software que a chama. Se o Servidor de Símbolos e o Servidor de Origem também são necessários, o SymSrv.dll e o SrcSrv.dll devem ser instalados no mesmo diretório que o DbgHelp.dll, pois DbgHelp só chamará essas DLLs se compartilharem o mesmo diretório com ele. (Observe que DbgHelp não chamará essas duas DLLs do caminho de pesquisa padrão.) Isso ajuda a evitar o uso de DLLs incompatibilidades; Da mesma forma, ele também melhora a segurança geral.

O código a seguir é extraído da origem DbgHelp. Ele mostra como DbgHelp carrega apenas versões do SymSrv.dll e SrcSrv.dll do mesmo diretório no qual DbgHelp.dll reside.


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



Depois de carregar essas duas DLLs, DbgHelp chama [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter as funções de que precisa delas.

Normalmente, o código que chama DbgHelp.dll garante que a versão correta seja carregada instalando DbgHelp.dll no mesmo diretório que o aplicativo que iniciou o processo atual. Se o código de chamada estiver em uma DLL e não tiver acesso ou conhecimento do local do processo inicial, o DbgHelp.dll deverá ser instalado junto com a DLL de chamada e o código semelhante à LoadDLL do DbgHelp deverá ser usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões do DbgHelp](dbghelp-versions.md)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**Getmodulefilename**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
