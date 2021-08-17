---
title: Para forçar Key-Frame inserção
description: Para forçar Key-Frame inserção
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- ASF (Advanced Systems Format), forçando inserções de quadro-chave
- ASF (Formato de Sistemas Avançados), forçando inserções de quadro-chave
- ASF (Advanced Systems Format), inserções de quadro-chave
- ASF (Formato de Sistemas Avançados), inserções de quadro-chave
- quadros chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d400c0ee4ba97aa7de559b1394dbe5c9fb2a974c124924aeae0839b1b4dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196492"
---
# <a name="to-force-key-frame-insertion"></a>Para forçar Key-Frame inserção

O codec Windows Media Video 9 dá suporte à inserção forçada de quadro-chave. Ao passar um exemplo para o autor, você pode especificar que ele deve ser codificado como um [*quadro-chave.*](wmformat-glossary.md)

Para forçar a inserção de quadro-chave para um exemplo, execute as etapas a seguir.

1.  Aloce um buffer para manter o exemplo e recupere um ponteiro para a interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) que contém o buffer chamando [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recupere o local e o tamanho do buffer criado na etapa 1 chamando [**INSSBuffer::GetBufferAndLength.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength)
3.  Copie seus dados de exemplo para o local do buffer, certificar-se de que o exemplo passado se ajustará ao buffer alocado. Dependendo da origem de seus exemplos, você pode usar uma variedade de funções para copiar os dados. Por exemplo, se você estiver copiando um fluxo de um arquivo AVI, poderá usar a função AVI, **AVIStreamRead.**
4.  Atualize a quantidade de dados usada no buffer para refletir o tamanho real do exemplo chamando [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Obtenha um ponteiro para a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) chamando **INSSBuffer::QueryInterface.**
6.  De definir o exemplo como um quadro-chave forçado chamando o [**método INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para definir a propriedade OutputCleanPoint do WM \_ SampleExtensionGUID. \_ Essa propriedade é um valor booliana; defini-lo como **TRUE.**
7.  Passe a interface de buffer para o autor juntamente com o número de entrada e o tempo de exemplo usando o [**método IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**Para gravar exemplos**](to-write-samples.md)
</dt> <dt>

[**Codificação de taxa de bits variável (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




