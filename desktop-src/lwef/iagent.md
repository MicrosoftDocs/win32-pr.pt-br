---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292194"
---
# <a name="iagent"></a>IAgent

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**IAgent** define uma interface que permite que os aplicativos carreguem caracteres, recebam eventos e verifiquem o estado atual do servidor do Microsoft Agent. Essas funções também estão disponíveis em [**IAgentEx**](iagentex.md).

O método getsuspended incluído nas versões anteriores é obsoleto e retorna **false** para compatibilidade com versões anteriores.

**Métodos em ordem vtable**



| Métodos IAgent                               | Descrição                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Carregar**](load-method.md)                  | Carrega o arquivo de dados de um caractere.                                |
| [**Liberação**](unload-method.md)              | Descarrega o arquivo de dados de um caractere.                              |
| [**Registre-se**](iagent--register.md)         | Registra um coletor de notificação para o cliente.                 |
| [**Unegister**](iagent--unregister.md)      | Cancela o registro do coletor de notificação de um cliente.                     |
| [**Getcharacter**](iagent--getcharacter.md) | Retorna a interface IAgentCharacter para um caractere carregado. |



 

 

 




