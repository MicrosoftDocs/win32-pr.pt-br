---
description: Inserção de quadro-chave forçada
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserção de quadro-chave forçada (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457213"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Inserção de quadro-chave forçada (Microsoft Media Foundation)

Ao configurar um objeto de codificador de vídeo, você pode definir um intervalo máximo para quadros-chave no conteúdo codificado. No entanto, o codec irá posicionar os quadros-chave dentro desse intervalo, conforme determinado pelo conteúdo; o intervalo de quadros chave não é constante. Para alguns aplicativos, a distância do quadro chave é muito importante. Por exemplo, um aplicativo de edição de vídeo precisa de quadros-chave em locais que são lógicos a um editor, como em quebras de cena e transições de captura.

A inserção de quadro-chave forçada é um recurso que permite solicitar que um quadro de entrada seja codificado como um quadro-chave. O codificador tentará respeitar essas solicitações, mas as configurações de buffer (taxa de bits e janela de buffer) configuradas para a sessão de codificação sempre terão precedência.

Os objetos do codificador de vídeo implementam a inserção de quadro chave forçado como uma resposta a uma extensão de unidade de dados anexada ao exemplo de entrada. Para obter mais informações sobre extensões de unidade de dados, consulte [usando extensões de unidade de dados](usingdataunitextensions.md).

Os dados de extensão para a inserção de quadro de chave forçada são identificados pelo seguinte valor de GUID: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. As extensões individuais são valores **bool** . Defina o valor como **true** para indicar uma solicitação de quadro-chave.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando extensões de unidade de dados](usingdataunitextensions.md)
</dt> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



