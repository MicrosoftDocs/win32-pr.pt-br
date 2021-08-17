---
description: Monitor de Rede usa a função de exportação DllMain para identificar a existência do analisador e liberar recursos que Monitor de Rede usa para armazenar informações sobre o analisador.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementando o analisador DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb79ab862c64d8d99359965fec6c0d1ca8bf3cf9e35fdf58f1cbc063d5c3e6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132935"
---
# <a name="implementing-dllmain-parser"></a>Implementando o analisador DllMain

Monitor de Rede usa a função de exportação **DllMain** para identificar a existência do analisador e liberar recursos que Monitor de Rede usa para armazenar informações sobre o analisador.

Quando Monitor de Rede chama **DllMain** pela primeira vez, a DLL do analisador chama [**CreateProtocol**](createprotocol.md) para fazer o seguinte:

-   Especifique o protocolo detectado pelo analisador.
-   Forneça pontos de entrada para funções de exportação restantes do analisador que Monitor de Rede chamadas.

Quando Monitor de Rede chama **DllMain** pela última vez, **dllMain** chama [**DestroyProtocol**](destroyprotocol.md) para liberar todos os recursos que Monitor de Rede usa para armazenar informações sobre o analisador.

O procedimento a seguir identifica as etapas necessárias para implementar **o DllMain**.

**Para implementar dllMain**

1.  [**Especifique a estrutura ENTRYPOINTS**](entrypoints.md) para a [**função CreateProtocol**](createprotocol.md) e a variável global Attach. A variável Attach é usada para acompanhar o número de instâncias de protocolo em execução.
2.  Veja o valor do parâmetro *Command* que o sistema operacional define.

    Se o parâmetro *Command* estiver definido como DLL PROCESS ATTACH e Attach for \_ 0, chame \_ [**CreateProtocol**](createprotocol.md) para fornecer o nome do protocolo e os pontos de entrada para as funções de exportação a seguir.

    -   **Registrar**
    -   **Cancelar registro**
    -   **RecognizeFrame**
    -   **AttachProperties**
    -   **FormatProperties** (necessário apenas se Monitor de Rede exibir as propriedades do protocolo).

    Se o *parâmetro Command* estiver definido como DLL PROCESS DETACH e Attach for 0, chame DestroyProtocol usando o handle de instância que \_ \_ [**CreateProtocol**](createprotocol.md) retorna. [](destroyprotocol.md)

3.  Retornar **TRUE** porque a função de analisador **DllMain** sempre deve retornar **TRUE.**

A seguir está uma implementação básica **de DllMain**. O exemplo de código usa uma instrução case para interceptar valores do parâmetro *Command* para determinar se [**CreateProtocol**](createprotocol.md) ou [**DestroyProtocol**](destroyprotocol.md) deve ser chamado.

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



