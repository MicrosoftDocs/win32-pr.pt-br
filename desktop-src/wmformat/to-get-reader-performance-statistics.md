---
title: Para obter estatísticas de desempenho do leitor
description: Para obter estatísticas de desempenho do leitor
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- ASF (Advanced Systems Format), estatísticas de desempenho de leitor
- ASF (formato de sistemas avançados), estatísticas de desempenho de leitor
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- Formato de sistema avançado (ASF), estatísticas de desempenho
- ASF (formato de sistemas avançados), estatísticas de desempenho
- leitores assíncronos, estatísticas de desempenho
- desempenho, estatísticas de leitor
- desempenho, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823562"
---
# <a name="to-get-reader-performance-statistics"></a>Para obter estatísticas de desempenho do leitor

Ao ler arquivos localmente com o leitor assíncrono, não é necessário verificar o desempenho das operações de leitura. No entanto, se seu aplicativo estiver lendo de uma fonte de streaming, as estatísticas de desempenho poderão ser muito importantes. Seu aplicativo pode responder às alterações no desempenho de reprodução para garantir a melhor experiência possível do usuário final.

As informações de desempenho que você pode recuperar do leitor incluem as seguintes estatísticas:

-   A largura de banda atual da conexão.
-   O número de pacotes recebidos do servidor.
-   O número de pacotes perdidos que foram recuperados.
-   O número de pacotes perdidos que não foram recuperados.
-   A porcentagem do número total de pacotes enviados que foram recebidos.

Para obter estatísticas de desempenho do leitor, execute as etapas a seguir.

1.  Antes de iniciar a reprodução, crie uma estrutura de [**\_ \_ estatísticas do WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) . Você deve definir o membro **cbSize** como sizeof (estatísticas do WM \_ Reader \_ ).
2.  Obtenha um ponteiro para a interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) do objeto leitor chamando **IWMReader:: QueryInterface**.
3.  Durante a reprodução, faça chamadas para [**IWMReaderAdvanced:: Getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) com frequência para monitorar o desempenho. Passe sua estrutura de **\_ \_ estatísticas do WM Reader** com cada chamada e examine os membros apropriados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




