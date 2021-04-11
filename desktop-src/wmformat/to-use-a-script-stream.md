---
title: Para usar um fluxo de script
description: Para usar um fluxo de script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- SDK do Windows Media Format, fluxos de script
- ASF (Advanced Systems Format), fluxos de script
- ASF (formato de sistemas avançados), fluxos de script
- fluxos de script, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292828"
---
# <a name="to-use-a-script-stream"></a>Para usar um fluxo de script

Esta seção descreve como enviar dados de script para o gravador para inclusão em um arquivo. Para obter informações sobre como incluir fluxos de script em perfis, consulte [Configurando tipos de fluxo arbitrários](configuring-arbitrary-stream-types.md).

Cada script consiste em duas cadeias de caracteres, um *tipo* String e uma cadeia de caracteres de *argumento* .

Os dados de script devem ser formatados antes de serem enviados ao gravador. As cadeias de caracteres devem ser concatenadas, separadas por um caractere **nulo** e terminadas com um caractere **nulo** . O exemplo a seguir mostra um script legítimo:



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | \\0 | h   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | um   | d   | um   | t   | u   | m   | .   | c   | o   | m   | \\0 |



 

Cada par de comandos de script deve ser escrito como um exemplo para o gravador. Para obter mais informações sobre como escrever exemplos, consulte [para escrever exemplos](to-write-samples.md).

Quando o arquivo ASF for reproduzido, os comandos de script serão entregues pelo leitor (ou leitor síncrono) na ordem de tempo da apresentação. É responsabilidade do aplicativo analisar as duas cadeias de caracteres e responder ao comando de script.

> [!Note]  
> Ao usar o DRM para criptografar um arquivo, nenhum comando de script pode ter um horário de apresentação de 0.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




