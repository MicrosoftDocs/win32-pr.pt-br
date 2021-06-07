---
title: Para usar um fluxo de script
description: Para usar um fluxo de script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, fluxos de script
- FORMATO DE SISTEMAS Avançados (ASF), fluxos de script
- ASF (Formato de Sistemas Avançados), fluxos de script
- fluxos de script, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444727"
---
# <a name="to-use-a-script-stream"></a>Para usar um fluxo de script

Esta seção descreve como enviar dados de script para o autor para inclusão em um arquivo. Para obter informações sobre como incluir fluxos de script em perfis, consulte [Configurando tipos de fluxo arbitrários](configuring-arbitrary-stream-types.md).

Cada script consiste em duas cadeias de caracteres, uma cadeia de caracteres *de* tipo e uma cadeia *de caracteres de* argumento.

Os dados de script devem ser formatados antes de serem enviados ao autor. As cadeias de caracteres devem ser concatenadas, separadas por um **caractere NULL** e terminadas com um **caractere NULL.** O exemplo a seguir mostra um script legítimo:



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | &nbsp; | h   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | um   | d   | um   | t   | u   | m   | .   | c   | o   | m   | &nbsp; |



 

Cada par de comandos de script deve ser gravado como um exemplo para o autor. Para obter mais informações sobre como escrever exemplos, consulte [To Write Samples](to-write-samples.md).

Quando o arquivo ASF for tocado, os comandos de script serão entregues pelo leitor (ou leitor síncrono) na ordem de tempo de apresentação. É responsabilidade do aplicativo analisar as duas cadeias de caracteres e responder ao comando de script.

> [!Note]  
> Ao usar o DRM para criptografar um arquivo, nenhum comando de script pode ter um tempo de apresentação de 0.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




