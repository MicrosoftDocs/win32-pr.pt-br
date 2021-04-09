---
description: Normalmente, os serviços são escritos como aplicativos de console.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Ponto de entrada de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9e2683c4a69949b6f51c7d000c0ee3571fe118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920845"
---
# <a name="service-entry-point"></a>Ponto de entrada de serviço

Normalmente, os serviços são escritos como aplicativos de console. O ponto de entrada de um aplicativo de console é sua função **principal** . A função **Main** recebe argumentos do valor **ImagePath** da chave do registro para o serviço. Para obter mais informações, consulte a seção comentários da função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .

Quando o SCM inicia um programa de serviço, ele aguarda que ele chame a função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) . Use as diretrizes a seguir.

-   Um serviço do tipo \_ \_ próprio processo do Win32 \_ deve chamar [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) imediatamente, de seu thread principal. Você pode executar qualquer inicialização depois que o serviço for iniciado, conforme descrito em [função Service-Main](service-servicemain-function.md).
-   Se o tipo de serviço for o \_ processo de compartilhamento Win32 do serviço \_ \_ e houver inicialização comum para todos os serviços no programa, você poderá executar a inicialização no thread principal antes de chamar [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), desde que demore menos de 30 segundos. Caso contrário, você deve criar outro thread para fazer a inicialização comum, enquanto o thread principal chama **StartServiceCtrlDispatcher**. Você ainda deve executar qualquer inicialização específica do serviço depois que o serviço for iniciado.

A função [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) usa uma estrutura de [**\_ \_ entrada de tabela de serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) para cada serviço contido no processo. Cada estrutura especifica o nome do serviço e o ponto de entrada para o serviço. Para obter um exemplo, consulte [escrevendo a função principal de um programa de serviço](writing-a-service-program-s-main-function.md).

Se [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) tiver sucesso, o thread de chamada não retornará até que todos os serviços em execução no processo tenham inserido o \_ estado serviço parado. O SCM envia solicitações de controle para esse thread por meio de um pipe nomeado. O thread atua como um Dispatcher de controle, executando as seguintes tarefas:

-   Crie um novo thread para chamar o ponto de entrada apropriado quando um novo serviço for iniciado.
-   Chame a [função de manipulador](service-control-handler-function.md) apropriada para manipular solicitações de controle de serviço.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo a função main de um programa de serviço](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



