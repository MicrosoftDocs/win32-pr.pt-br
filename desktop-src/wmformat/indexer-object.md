---
title: Objeto indexador
description: Objeto indexador
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows SDK do formato de mídia, objetos do indexador
- ASF (Advanced Systems Format), objetos indexador
- ASF (formato de sistemas avançados), objetos do indexador
- objetos, objetos indexador
- objetos do indexador
- índices, objetos indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795ef166f6b3ad46897305cbd3f6c38bbc7a219bb99df1dcf8b14dbfb1443577
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839783"
---
# <a name="indexer-object"></a>Objeto indexador

O objeto indexador cria um índice em um arquivo ASF. Um índice é uma parte padrão de um arquivo ASF que equipara amostras de vídeo com horas, números de quadro ou (se aplicável) os carimbos de hora padrão da sociedade de imagem e dos engenheiros de televisão (SMPTE). Sem um índice, nem o objeto leitor nem o objeto leitor síncrono podem buscar um ponto no meio de um arquivo.

Os índices criados por esse objeto só serão necessários se o arquivo contiver um ou mais fluxos de vídeo. Isso ocorre porque os dados de áudio não são compactados de forma temporal, facilitando a localização de um determinado tempo em um fluxo de áudio.

O objeto indexador é criado pela função [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , que define um ponteiro para uma interface **IWMIndexer** . As outras interfaces do objeto indexador podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte do objeto indexador.



| Interface                          | Descrição                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | Inicia e para o processo de indexação.                                              |
| [**IWMIndexer2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | Configura o indexador, habilitando a indexação por quadro, por hora ou pelo código de tempo SMPTE. |



 

A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para usar o objeto indexador.



| Interface                                      | Descrição                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Recebe mensagens de status de processos que são executados em um thread separado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto**](objects.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




