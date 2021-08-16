---
title: Para buscar por tempo usando o leitor assíncrono
description: Para buscar por tempo usando o leitor assíncrono
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- ASF (Advanced Systems Format), buscando por tempo
- ASF (Formato de Sistemas Avançados), buscando por tempo
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (Formato de Sistemas Avançados), leitores assíncronos
- leitores assíncronos, buscando por tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d480cade395cdbead99b1aedde8928c6fb18b4af15bf6b72c1bcc0dcd6dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196455"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>Para buscar por tempo usando o leitor assíncrono

Se você quiser buscar uma hora de apresentação específica em um arquivo ASF, o arquivo deverá ser configurado corretamente. Você pode buscar apenas arquivos de áudio por padrão, mas os arquivos de vídeo precisam ser indexados antes de serem buscados. Se você não tiver certeza sobre como um arquivo foi criado, poderá verificar o atributo g wszWMSeekable no título do arquivo chamando \_ [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).

Para buscar dados em um arquivo ASF por tempo de apresentação usando o leitor assíncrono, chame [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passando a hora e a duração desejadas da parte do arquivo que você deseja ler como *cnsStart* e *cnsDuration,* respectivamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lendo arquivos com o Leitor Assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lendo metadados na reprodução**](reading-metadata-at-playback.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




