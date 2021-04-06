---
description: Monitor de Rede usa a função de exportação DllMain para identificar a existência do analisador e liberar os recursos que o Monitor de Rede usa para armazenar informações sobre o analisador.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementando o analisador DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646787"
---
# <a name="implementing-dllmain-parser"></a>Implementando o analisador DllMain

Monitor de Rede usa a função de exportação **DllMain** para identificar a existência do analisador e liberar os recursos que o monitor de rede usa para armazenar informações sobre o analisador.

Quando Monitor de Rede chama **DllMain** pela primeira vez, a DLL do analisador chama [**createprotocol**](createprotocol.md) para fazer o seguinte:

-   Especifique o protocolo que o analisador detecta.
-   Forneça pontos de entrada para as funções de exportação do analisador restantes que Monitor de Rede chamadas.

Quando Monitor de Rede chama **DllMain** pela última vez, **DllMain** chama [**DestroyProtocol**](destroyprotocol.md) para liberar todos os recursos que monitor de rede usa para armazenar informações sobre o analisador.

O procedimento a seguir identifica as etapas necessárias para implementar o **DllMain**.

**Para implementar o DllMain**

1.  Especifique a estrutura de [**entryPoints**](entrypoints.md) para a função [**createprotocol**](createprotocol.md) e a variável de anexação global. A variável de anexação é usada para rastrear o número de instâncias de protocolo que estão em execução.
2.  Examine o valor do parâmetro de *comando* definido pelo sistema operacional.

    Se o parâmetro de *comando* for definido como dll do \_ processo \_ anexar e anexar for 0, chame [**createprotocol**](createprotocol.md) para fornecer o nome do protocolo e os pontos de entrada para as seguintes funções de exportação.

    -   **Registrar**
    -   **Cancelar registro**
    -   **RecognizeFrame**
    -   **Anexarproperties**
    -   **Formatproperties** (obrigatório somente se monitor de rede exibir as propriedades de protocolo).

    Se o parâmetro de *comando* for definido como \_ dll \_ , desanexar e anexar é 0, chame [**DestroyProtocol**](destroyprotocol.md) usando o identificador de instância que o [**createprotocol**](createprotocol.md) retorna.

3.  Retornar **true** porque a função do analisador **DllMain** sempre deve retornar **true**.

A seguir está uma implementação básica do **DllMain**. O exemplo de código usa uma instrução Case para interceptar valores do parâmetro *Command* para determinar se [**createprotocol**](createprotocol.md) ou [**DestroyProtocol**](destroyprotocol.md) devem ser chamados.

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

 

 



