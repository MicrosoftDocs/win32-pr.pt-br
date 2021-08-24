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
ms.openlocfilehash: 4b51b46f3efdf95902b1ca5b359227da845292c4b0f23dbf0bd52039fba151cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029067"
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

 

 




