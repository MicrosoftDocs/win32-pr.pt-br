---
title: Enumeração de formato de entrada
description: Enumeração de formato de entrada
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- SDK do Windows Media Format, enumerações de formato de entrada
- SDK do Windows Media Format, enumerando formatos de entrada
- ASF (Advanced Systems Format), enumerações de formato de entrada
- ASF (formato de sistemas avançados), enumerações de formato de entrada
- Formato de sistema avançado (ASF), enumerando formatos de entrada
- ASF (formato de sistemas avançados), enumerando formatos de entrada
- enumerações de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453709"
---
# <a name="input-format-enumeration"></a>Enumeração de formato de entrada

O objeto Writer Obtém informações de formato de fluxo do perfil que você fornece. As informações de configuração de fluxo em um perfil fornecem ao escritor todas as informações necessárias sobre como os dados devem ser gravados no arquivo. O perfil não fornece ao gravador nenhuma informação sobre o formato dos exemplos de entrada que seu aplicativo fornece. Os formatos de entrada serão desconhecidos somente para fluxos compactados com um dos codecs de mídia do Windows; as entradas para tipos de fluxo arbitrários são previsíveis com base nas informações no perfil.

O objeto Writer pode se comunicar com o codec de um fluxo para determinar os tipos de entrada que podem ser usados. Os métodos são fornecidos para enumerar os tipos de entrada possíveis. Você sempre deve encontrar o tipo de entrada que corresponde à sua mídia de entrada enumerando os tipos com suporte em vez de definir as propriedades de mídia de entrada manualmente. Para obter mais informações, consulte [para enumerar formatos de entrada](to-enumerate-input-formats.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de gravação de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> </dl>

 

 




