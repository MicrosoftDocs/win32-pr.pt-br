---
title: Coletores
description: Coletores
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- SDK do Windows Media Format, coletores
- SDK do Windows Media Format, coletores de arquivos
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- ASF (Advanced Systems Format), coletores de arquivos
- ASF (formato de sistemas avançados), coletores de arquivo
- SDK do Windows Media Format, coletores de rede
- SDK do Windows Media Format, coletores push
- ASF (Advanced Systems Format), coletores de rede
- ASF (formato de sistemas avançados), coletores de rede
- ASF (Advanced Systems Format), coletores push
- ASF (formato de sistemas avançados), coletores push
- coletores, sobre
- coletores de arquivos, sobre
- coletores de rede
- coletores push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007136"
---
# <a name="sinks"></a>Coletores

O objeto do gravador do Windows Media Format SDK fornece conteúdo processado para coletores. Cada coletor é um objeto que entrega dados. O ponto de entrega depende do tipo de coletor. Há três tipos de coletores: coletores de arquivos, coletores de rede e coletores de push.

## <a name="file-sinks"></a>Coletores de arquivos

Coletores de arquivos gravam conteúdo ASF em um arquivo em uma unidade local ou de rede. Quando você usa o objeto Writer para gravar um arquivo sem adicionar explicitamente um coletor de arquivos, o gravador criará um para você usando o nome passado para [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename). Você pode atribuir vários coletores de arquivo a um objeto gravador para gravar o conteúdo em vários arquivos ao mesmo tempo.

Usando um coletor de arquivos, você pode controlar vários aspectos do arquivo. Os recursos a seguir estão disponíveis por meio de um coletor de arquivos.

-   Monitoramento de estatísticas de arquivo. Você pode monitorar o tamanho do arquivo e a duração à medida que ele está sendo criado.
-   Criação de arquivo de conteúdo parcial. Os coletores de arquivos podem ser configurados para começar a gravar conteúdo em um horário específico e para terminar a gravação em um horário específico. Isso permite que você crie vários arquivos que contenham seções diferentes do mesmo conteúdo na mesma passagem de escrita.

## <a name="network-sinks"></a>Coletores de rede

Coletores de rede difundem o conteúdo para um endereço de rede. A leitura de clientes pode se conectar ao endereço para receber a transmissão.

## <a name="push-sinks"></a>Coletores push

Coletores Push entregam conteúdo do gravador para um servidor que executa os serviços de mídia do Windows. Os coletores de push normalmente são usados em cenários em que um computador codifica conteúdo ao vivo e o entrega a um ou mais servidores para distribuição ampla. O uso de um coletor de push permite dedicar computadores a tarefas específicas, economizando largura de banda e capacidade de processamento em cada servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de gravação de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> </dl>

 

 




