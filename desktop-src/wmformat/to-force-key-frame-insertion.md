---
title: Para forçar a inserção de Key-Frame
description: Para forçar a inserção de Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- ASF (Advanced Systems Format), forçando inserções de quadros-chave
- ASF (formato de sistemas avançados), forçando inserções de quadros-chave
- ASF (Advanced Systems Format), inserções de quadro-chave
- ASF (formato de sistemas avançados), inserções de quadros-chave
- quadros chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104453883"
---
# <a name="to-force-key-frame-insertion"></a>Para forçar a inserção de Key-Frame

O codec Windows Media Video 9 dá suporte à inserção forçada de quadros-chave. Ao passar um exemplo para o gravador, você pode especificar que ele deve ser codificado como um [*quadro-chave*](wmformat-glossary.md).

Para forçar a inserção de quadro-chave para um exemplo, execute as etapas a seguir.

1.  Aloque um buffer para manter o exemplo e recupere um ponteiro para a interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) que contém o buffer chamando [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recupere o local e o tamanho do buffer criado na etapa 1 chamando [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).
3.  Copie os dados de exemplo para o local do buffer, certificando-se de que o exemplo passado caiba no buffer alocado. Dependendo da origem de seus exemplos, você pode usar uma variedade de funções para copiar os dados. Por exemplo, se você estiver copiando um fluxo de um arquivo AVI, poderá usar a função AVI, **AVIStreamRead**.
4.  Atualize a quantidade de dados usados no buffer para refletir o tamanho real do exemplo chamando [**INSSBuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Obtenha um ponteiro para a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) chamando **INSSBuffer:: QueryInterface**.
6.  Defina o exemplo como um quadro-chave forçado chamando o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para definir a \_ Propriedade OutputCleanPoint do WM SampleExtensionGUID \_ . Esta propriedade é um valor booliano; Defina-o como **true**.
7.  Passe a interface de buffer para o gravador junto com o número de entrada e o tempo de amostra usando o método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**Para escrever exemplos**](to-write-samples.md)
</dt> <dt>

[**Codificação de taxa de bits variável (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




