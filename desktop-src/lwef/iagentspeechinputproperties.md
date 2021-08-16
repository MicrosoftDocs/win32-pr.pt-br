---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660848eae85465ea322bcb08a218c6ee463eb384d3a4766cacf6a86038662386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609326"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O IAgentSpeechInputProperties fornece acesso às propriedades de entrada de fala mantidas pelo servidor. A maioria das propriedades é somente leitura para aplicativos cliente, mas o usuário pode alterá-las na folha de propriedades do Microsoft Agent. O servidor do Microsoft Agent retornará valores somente se um mecanismo de fala compatível tiver sido instalado e estiver habilitado. A consulta dessas propriedades tenta iniciar o mecanismo de fala.

**Métodos em ordem vtable**



| Métodos IAgentSpeechInputProperties                                     | Descrição                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**GetEnabled**](iagentspeechinputproperties--getenabled.md)           | Retorna se o mecanismo de reconhecimento de fala está habilitado. |
| [**Gettecla de atalho**](iagentspeechinputproperties--gethotkey.md)             | Retorna a atribuição de chave atual da chave de escuta.  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | Retorna se a dica de escuta está habilitada.             |



 

Os métodos [**Getinstaled**](https://www.bing.com/search?q=**GetInstalled**), [**getlcid**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)e [**setengine**](https://www.bing.com/search?q=**SetEngine**) (com suporte em versões anteriores do Microsoft Agent) ainda têm suporte para compatibilidade com versões anteriores. No entanto, os métodos não são fragmentado e não retornam valores úteis. Use [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) e [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) para consultar e definir o mecanismo de reconhecimento de fala a ser usado com o caractere. Tenha em mente que o mecanismo deve corresponder à configuração de idioma atual do caractere.

 

 




