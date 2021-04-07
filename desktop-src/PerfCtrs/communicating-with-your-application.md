---
description: Normalmente, um provedor fornece dados em nome de um aplicativo.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicando-se com seu aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828395"
---
# <a name="communicating-with-your-application"></a>Comunicando-se com seu aplicativo

Normalmente, um provedor fornece dados em nome de um aplicativo. Por exemplo, um servidor pode criar uma DLL de desempenho para fornecer seus dados de contador. A comunicação entre um aplicativo e seu provedor é diferente para o modo de usuário e aplicativos de modo kernel. Provedores são executados no modo de usuário. Por causa disso, aplicativos de modo de usuário, como aplicativos de impressão e exibição, podem usar qualquer técnica para comunicação entre processos, como pipes nomeados, mapeamento de arquivos ou RPC. No entanto, os aplicativos em modo kernel devem fornecer uma interface IOCTL que retorna os dados de desempenho para o provedor.

> [!WARNING]
> Não use COM como o mecanismo IPC. O sistema não pode garantir o estado de inicialização COM do thread que chama a interface. Portanto, a DLL pode não conseguir inicializar com e coletar os dados com êxito.

 

 

 



