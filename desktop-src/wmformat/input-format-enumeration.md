---
title: Enumeração de formato de entrada
description: Enumeração de formato de entrada
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows SDK de Formato de Mídia, enumerações de formato de entrada
- Windows SDK de Formato de Mídia, enumerando formatos de entrada
- FORMATO DE SISTEMAS Avançados (ASF), enumerações de formato de entrada
- ASF (Formato de Sistemas Avançados), enumerações de formato de entrada
- ASF (Advanced Systems Format), enumerando formatos de entrada
- ASF (Formato de Sistemas Avançados), enumerando formatos de entrada
- enumerações de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a261b2edae285a970bead5d039c4e85076530eb363aa025289b75ec56618406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809036"
---
# <a name="input-format-enumeration"></a>Enumeração de formato de entrada

O objeto writer obtém informações de formato de fluxo do perfil que você lhe dá. Transmitir informações de configuração em um perfil fornece ao autor todas as informações necessárias sobre como os dados devem ser gravados no arquivo. O perfil não fornece ao autor nenhuma informação sobre o formato dos exemplos de entrada que seu aplicativo fornece. Os formatos de entrada serão desconhecidos somente para fluxos compactados com um dos codecs Windows Media; entradas para tipos de fluxo arbitrários são previsíveis com base nas informações no perfil.

O objeto writer pode se comunicar com o codec de um fluxo para determinar os tipos de entrada que podem ser usados. Métodos são fornecidos para enumerar os tipos de entrada possíveis. Você sempre deve encontrar o tipo de entrada que corresponde à mídia de entrada enumerando os tipos com suporte em vez de definir as propriedades da mídia de entrada manualmente. Para obter mais informações, consulte [Para enumerar formatos de entrada](to-enumerate-input-formats.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de escrita de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> </dl>

 

 




