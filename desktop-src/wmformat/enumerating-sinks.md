---
title: Enumerando coletores
description: Enumerando coletores
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- ASF (Advanced Systems Format), enumerando coletores
- ASF (formato de sistemas avançados), enumerando coletores
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, enumerando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103640281"
---
# <a name="enumerating-sinks"></a>Enumerando coletores

O gravador pode ter muitos coletores associados a ele. Você pode enumerar os coletores que foram adicionados ao gravador usando [**IWMWriterAdvanced:: GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) e [**IWMWriterAdvanced:: getsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).

O código de exemplo na [obtenção de mensagens de erro de um coletor demonstra a enumeração do](getting-error-messages-from-a-sink.md) coletor.

> [!Note]  
> Ao enumerar coletores, o coletor de arquivo padrão criado em resposta a uma chamada para [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) será enumerado junto com outros coletores que você adicionou. Se você estiver usando apenas o coletor de arquivos padrão, poderá acessá-lo chamando **getsink** para o índice de coletor 0.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> </dl>

 

 




