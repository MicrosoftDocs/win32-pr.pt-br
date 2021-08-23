---
description: Normalmente, um provedor fornece dados em nome de um aplicativo.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicando-se com seu aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb696c0c12ed8de542b07067fe16e13c9c098cb712393975e82d948bc3238979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061224"
---
# <a name="communicating-with-your-application"></a>Comunicando-se com seu aplicativo

Normalmente, um provedor fornece dados em nome de um aplicativo. Por exemplo, um servidor pode criar uma DLL de desempenho para fornecer seus dados de contador. A comunicação entre um aplicativo e seu provedor difere para aplicativos no modo de usuário e no modo kernel. Os provedores são executados no modo de usuário. Por isso, os aplicativos de modo de usuário, como aplicativos de impressão e exibição, podem usar qualquer técnica para comunicação entre processos, como pipes nomeados, mapeamento de arquivos ou RPC. No entanto, os aplicativos no modo kernel devem fornecer uma interface IOCTL que retorna os dados de desempenho para o provedor.

> [!WARNING]
> Não use COM como o mecanismo IPC. O sistema não pode garantir o estado de inicialização COM do thread que chama a interface. Portanto, a DLL pode não ser capaz de inicializar com êxito o COM e coletar os dados.

 

 

 



