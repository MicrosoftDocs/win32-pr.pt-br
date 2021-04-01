---
description: Criando filtros do DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Criando filtros do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5553c4358f97809214ebbdea23c129aa7c214e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646042"
---
# <a name="building-directshow-filters"></a>Criando filtros do DirectShow

As classes base do DirectShow são recomendadas para a implementação de filtros do DirectShow. Para criar com as classes base, execute as etapas a seguir, além das etapas listadas em [Configurando o ambiente de compilação](setting-up-the-build-environment.md):

-   Crie a biblioteca de classes base, localizada no diretório Samples \\ Multimedia \\ DirectShow \\ BaseClasses, no diretório raiz do SDK. Há duas versões da biblioteca: uma versão comercial (Strmbase. lib) e uma versão de depuração (Strmbasd. lib).
-   Inclua o cabeçalho file Streams. h.
-   Use a \_ \_ Convenção de chamada stdcall.
-   Use a biblioteca de tempo de execução C multithread (depuração ou varejo, conforme apropriado).
-   Inclua um arquivo de definição (. def) que exporta as funções de DLL. Veja a seguir um exemplo de um arquivo de definição. Ele pressupõe que o arquivo de saída é nomeado MyFilter.dll.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Link para os seguintes arquivos lib.

    |              |                                      |
    |--------------|--------------------------------------|
    | Depurar compilação  | Strmbasd. lib, MSVCRTD. lib, winmm. lib |
    | Build de varejo | Strmbase. lib, msvcrt. lib, winmm. lib  |

    

     

-   Escolha a opção "ignorar bibliotecas padrão" nas configurações do vinculador.
-   Declare o ponto de entrada de DLL em seu código-fonte, da seguinte maneira:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Versões anteriores

Para versões da biblioteca de classes base antes do DirectShow 9,0, você também deve fazer o seguinte:

-   Para compilações de depuração, defina a depuração do sinalizador de pré-processador.

Esta etapa não é necessária para a versão da biblioteca de classes base que está disponível no DirectShow 9,0 e posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes base do DirectShow](directshow-base-classes.md)
</dt> <dt>

[Gravando filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



