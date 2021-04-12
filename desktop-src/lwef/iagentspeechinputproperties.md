---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363622"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O IAgentSpeechInputProperties fornece acesso às propriedades de entrada de fala mantidas pelo servidor. A maioria das propriedades é somente leitura para aplicativos cliente, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent. O servidor do Microsoft Agent retornará valores somente se um mecanismo de fala compatível tiver sido instalado e estiver habilitado. A consulta dessas propriedades tenta iniciar o mecanismo de fala.

**Métodos em ordem vtable**



| Métodos IAgentSpeechInputProperties                                     | Descrição                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**GetEnabled**](iagentspeechinputproperties--getenabled.md)           | Retorna se o mecanismo de reconhecimento de fala está habilitado. |
| [**Gettecla de atalho**](iagentspeechinputproperties--gethotkey.md)             | Retorna a atribuição de chave atual da chave de escuta.  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | Retorna se a dica de escuta está habilitada.             |



 

Os métodos [**Getinstaled**](https://www.bing.com/search?q=**GetInstalled**), [**getlcid**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)e [**setengine**](https://www.bing.com/search?q=**SetEngine**) (com suporte em versões anteriores do Microsoft Agent) ainda têm suporte para compatibilidade com versões anteriores. No entanto, os métodos não são fragmentado e não retornam valores úteis. Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) e [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) para consultar e definir o mecanismo de reconhecimento de fala a ser usado com o caractere. Tenha em mente que o mecanismo deve corresponder à configuração de idioma atual do caractere.

 

 




