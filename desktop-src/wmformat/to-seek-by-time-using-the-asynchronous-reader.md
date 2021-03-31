---
title: Para procurar por tempo usando o leitor assíncrono
description: Para procurar por tempo usando o leitor assíncrono
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- ASF (Advanced Systems Format), buscando por tempo
- ASF (formato de sistemas avançados), buscando por tempo
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, buscando por tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640162"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Para procurar por tempo usando o leitor assíncrono

Se você quiser buscar um tempo de apresentação específico em um arquivo ASF, o arquivo deverá ser configurado corretamente. Você pode buscar apenas arquivos de áudio por padrão, mas os arquivos de vídeo precisam ser indexados antes de procurar. Se você não tiver certeza de como um arquivo foi criado, poderá verificar o \_ atributo g wszWMSeekable no cabeçalho do arquivo chamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Para buscar dados em um arquivo ASF por hora de apresentação usando o leitor assíncrono, chame [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passando a hora desejada e a duração da parte do arquivo que você deseja ler como *cnsStart* e *cnsDuration* , respectivamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lendo metadados na reprodução**](reading-metadata-at-playback.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




