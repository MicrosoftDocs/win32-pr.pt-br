---
title: Objeto de buffer
description: Objeto de buffer
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- SDK do Windows Media Format, objetos de buffer
- Formato de sistema avançado (ASF), objetos de buffer
- ASF (formato de sistemas avançados), objetos de buffer
- objetos, objetos de buffer
- objetos de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105782691"
---
# <a name="buffer-object"></a>Objeto de buffer

Um objeto buffer é usado para manter amostras e fornecê-los entre os objetos do Windows Media Format SDK e seu aplicativo. Ao gravar um arquivo, você passa seus exemplos de entrada para o gravador usando objetos de buffer. Quando você lê um arquivo, o objeto leitor ou o objeto leitor síncrono fornece amostras para seu aplicativo em objetos de buffer.

Para escrever exemplos em um arquivo, você pode criar um objeto de buffer usando o método [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) . Para exemplos de leitura, o objeto leitor e o objeto leitor síncrono criam objetos de buffer internamente. Se você optar pelo, poderá alocar seus próprios objetos de buffer para leitura de arquivo usando [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) ou [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).

As interfaces a seguir têm suporte em cada objeto de buffer.



| Interface                          | Descrição                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | Controla e fornece acesso ao buffer.                          |
| [**INSSBuffer2**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | Não implementado.                                                     |
| [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | Dá suporte a propriedades de buffer, que são usadas para extensões de unidade de dados. |
| [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | Enumera as propriedades do buffer.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> </dl>

 

 




