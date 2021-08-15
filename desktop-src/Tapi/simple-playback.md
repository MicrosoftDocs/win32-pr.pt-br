---
description: O tópico a seguir descreve como executar a reprodução simples.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Reprodução simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51724b92fea0a46850609e96de85231a9f1df1f7e538f6def4df07442ef19ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118862222"
---
# <a name="simple-playback"></a>Reprodução simples

O tópico a seguir descreve como executar a reprodução simples.

**Para executar a reprodução simples**

1.  Selecione o terminal de reprodução de arquivo no nível de chamada.
2.  Crie o terminal de reprodução na chamada TAPI.
3.  Definir propriedades — nome do arquivo e tipo de armazenamento.
4.  Chame o método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) no terminal de reprodução de arquivos para iniciar a reprodução de fluxos.

O código de exemplo a seguir demonstra a reprodução simples.

Primeiro, use a interface [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) para criar o terminal para gravação. Isso instrui o TSP/MSP a executar a reprodução de arquivos nessa chamada. O TSP/MSP cria um terminal para o aplicativo usar e o retorna em caso de sucesso.


```C++

```



Obtenha o ponteiro de interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) da interface do terminal e use-o para definir o nome do arquivo a ser reproduzido.


```C++
pMediaPlayback->Release();
```



Supondo que o arquivo contenha um fluxo de áudio e a chamada tenha um fluxo de áudio de captura, o conteúdo de áudio no arquivo será reproduzido nesse fluxo.

 

 



