---
title: Desenvolvendo o servidor
description: Ao criar um programa de servidor para um aplicativo distribuído, você deve usar o arquivo de cabeçalho e o stub de servidor que o compilador de MIDL gera.
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- Chamada de procedimento remoto RPC, tarefas, desenvolvendo o servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efeba77168abe53e1df823f416c80a015cc63bc7b89c79a0a86d79174a7c78fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073396"
---
# <a name="developing-the-server"></a>Desenvolvendo o servidor

Ao criar um programa de servidor para um aplicativo distribuído, você deve usar o arquivo de cabeçalho e o stub de servidor que o compilador de MIDL gera. Para obter detalhes, consulte [desenvolvendo a interface](developing-the-interface.md). Inclua o arquivo de cabeçalho no arquivo de programa do servidor C. Compile o stub do servidor com os arquivos de origem C que compõem seu aplicativo. Vincule os arquivos de objeto resultantes com a biblioteca de importação. Esse processo é ilustrado no diagrama a seguir.

![processo de criação de um programa de servidor para um aplicativo distribuído](images/srvrdev.png)

Como você pode ver no exemplo na ilustração, um arquivo MIDL chamado MyApp. idl foi usado para definir a interface. O compilador MIDL usou MyApp. idl para produzir MyApp \_ s. c e MyApp. h. Ele também produz um arquivo de origem C para o stub do cliente, mas isso não é relevante para essa discussão específica. O arquivo de origem C para o programa de servidor (nesse caso, Mysrvr. C) deve incluir o arquivo MyApp. h. Também será necessário incluir os arquivos RPC. h e Rpcndr. h.

O aplicativo de servidor foi desenvolvido em dois arquivos, Mysrvr. c e Rprocs. c. O arquivo Mysrvr. c contém as funções necessárias para colocar o programa do servidor em funcionamento. Os procedimentos remotos que o programa do servidor oferece estão contidos no arquivo Rprocs. c.

Os arquivos Mysrvr. c e Rprocs. c foram compilados junto com MyApp \_ s. c para produzir arquivos de objeto. Os arquivos de objeto foram então vinculados com a biblioteca de tempo de execução RPC e quaisquer outras bibliotecas que possam precisar. O resultado é um programa de servidor executável chamado Mysrvr.exe.

Se você não compilar seu arquivo IDL no modo de compatibilidade do uso (Open Software Foundation) ([**/OSF**](/windows/desktop/Midl/-osf)), o programa do servidor deverá fornecer uma função para alocar memória e uma função para desalocá-lo. para Windows 2000 e versões posteriores do Windows, o modo recomendado é [**/Oicf**](/windows/desktop/Midl/-oi). Para obter detalhes, consulte [como a memória é alocada e desalocada](how-memory-is-allocated-and-deallocated.md), e [ponteiros e alocação de memória](pointers-and-memory-allocation.md).

 

 