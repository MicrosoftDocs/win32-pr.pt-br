---
description: Inserção forçada de quadro-chave
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserção forçada de quadro-chave (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9790a40c7fc6d2248377003005bbff7ad56b54208e1d20814d5c8150223198ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466136"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Inserção forçada de quadro-chave (Microsoft Media Foundation)

Ao configurar um objeto de codificador de vídeo, você pode definir um intervalo máximo para quadros-chave no conteúdo codificado. No entanto, o codec colocará quadros-chave dentro desse intervalo, conforme ditado pelo conteúdo; O intervalo do quadro-chave não é constante. Para alguns aplicativos, a distância do quadro-chave é muito importante. Por exemplo, um aplicativo de edição de vídeo precisa de quadros-chave em locais lógicos para um editor, como em quebras de cena e transições de disparo.

A inserção forçada de quadro-chave é um recurso que permite solicitar que um quadro de entrada seja codificado como um quadro-chave. O codificador tentará aceitar essas solicitações, mas as configurações de buffer (taxa de bits e janela de buffer) configuradas para a sessão de codificação sempre têm precedência.

Os objetos do codificador de vídeo implementam a inserção forçada de quadro-chave como uma resposta a uma extensão de unidade de dados anexada ao exemplo de entrada. Para obter mais informações sobre extensões de unidade de dados, consulte [Usando extensões de unidade de dados](usingdataunitextensions.md).

Os dados de extensão para inserção forçada de quadro-chave são identificados pelo seguinte valor guid: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. As extensões individuais são **valores BOOL.** De definir o valor como **TRUE** para indicar uma solicitação de quadro-chave.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando extensões de unidade de dados](usingdataunitextensions.md)
</dt> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



