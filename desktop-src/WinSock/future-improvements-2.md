---
description: Melhorias futuras no código do aplicativo Winsock de exemplo.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Aprimoramentos futuros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384d5a4f4ee9a4d6cb4a0f258d63262930dc5a6636be8d0e7f709b0e4f04e152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132359"
---
# <a name="future-improvements"></a>Aprimoramentos futuros

Há várias melhorias que podem ser feitas nesse aplicativo, como:

-   Uma conexão única e persistente pode ser criada pelo aplicativo. O tratamento de erros apropriado teria que ser adicionado. Isso reduziria a sobrecarga associada à inicialização e à desmontagem da conexão.
-   O código de resposta no servidor pode ser otimizado para consolidar respostas, reduzindo o número de pacotes enviados do servidor.
-   As melhorias no protocolo podem ser feitas. Por exemplo, um bitmask de atualização poderia ser usado para significar quais células devem ser atualizadas e apenas os dados de célula enviados.
-   As atualizações podem ser sobrepostas usando threads diferentes, para que a rede não fique ociosa enquanto a função **ComputeNext** estiver em execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhorando um aplicativo lento](improving-a-slow-application-2.md)
</dt> <dt>

[A versão de linha de base: um aplicativo com muito mau desempenho](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisão 1: limpando o óbvio](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisão 2: redesignação para menos conexões](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisão 3: envio de bloco compactado](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



