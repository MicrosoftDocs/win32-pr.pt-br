---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3931c277fbe4a5943ef5881da12cf3669b2e8894c95052f61bc8411e21c7ae3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751420"
---
# <a name="iagent"></a>IAgent

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

**O IAgent** define uma interface que permite que os aplicativos carreguem caracteres, recebam eventos e verifiquem o estado atual do Microsoft Agent Server. Essas funções também estão disponíveis no [**IAgentEx.**](iagentex.md)

O método GetSuspended incluído nas versões anteriores é obsoleto e retorna **False para** compatibilidade com versões anteriores.

**Métodos em ordem Vtable**



| Métodos IAgent                               | Descrição                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Carregar**](load-method.md)                  | Carrega o arquivo de dados de um caractere.                                |
| [**Descarregar**](unload-method.md)              | Descarrega o arquivo de dados de um caractere.                              |
| [**Registrar**](iagent--register.md)         | Registra um sink de notificação para o cliente.                 |
| [**Não registro**](iagent--unregister.md)      | Unregisters a client's notification sink.                     |
| [**GetCharacter**](iagent--getcharacter.md) | Retorna a interface IAgentCharacter para um caractere carregado. |



 

 

 




