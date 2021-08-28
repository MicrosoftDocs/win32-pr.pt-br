---
description: Criando filtros DirectShow dados
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Criando filtros DirectShow dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d1983d3bfd42d1a1582ef696b6793acdd0856dde2bd2d589e809acc614314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794316"
---
# <a name="building-directshow-filters"></a>Criando filtros DirectShow dados

As DirectShow base de dados são recomendadas para implementar DirectShow filtros. Para criar com as classes base, execute as seguintes etapas, além das etapas listadas em [Configurando o Ambiente de Build](setting-up-the-build-environment.md):

-   Crie a biblioteca de classes base, localizada no diretório Samples \\ Multimedia \\ DirectShow \\ BaseClasses, no diretório raiz do SDK. Há duas versões da biblioteca: uma versão de varejo (Strmbase.lib) e uma versão de depuração (Strmbasd.lib).
-   Inclua o arquivo de Fluxos.h.
-   Use a \_ \_ convenção de chamada stdcall.
-   Use a biblioteca em tempo de run time C multithread (depuração ou varejo, conforme apropriado).
-   Inclua um arquivo de definição (.def) que exporta as funções DLL. A seguir está um exemplo de um arquivo de definição. Ele supõe que o arquivo de saída seja chamado MyFilter.dll.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Vincule aos seguintes arquivos lib.

| Rótulo | Valor |
    |--------------|--------------------------------------|
    | Build de depuração  | Strmbasd.lib, Msvcrtd.lib, Winmm.lib |
    | Build de varejo | Strmbase.lib, Msvcrt.lib, Winmm.lib  |

    

     

-   Escolha a opção "ignorar bibliotecas padrão" nas configurações do vinculador.
-   Declare o ponto de entrada DLL em seu código-fonte, da seguinte forma:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Versões anteriores

Para versões da biblioteca de classes base antes DirectShow 9.0, você também deve fazer o seguinte:

-   Para builds de depuração, defina o sinalizador de pré-processador DEBUG.

Esta etapa não é necessária para a versão da biblioteca de classes base que está disponível no DirectShow 9.0 e posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Base Classes](directshow-base-classes.md)
</dt> <dt>

[Escrevendo DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



