---
title: Criando arquivos ASF no DirectShow (Windows Media Format SDK 11)
description: Saiba mais sobre como criar arquivos ASF no DirectShow usando o SDK Windows Media Format 11. ASF é um formato de contêiner que pode conter qualquer tipo de dados.
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, criando arquivos ASF no DirectShow
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), criando no DirectShow
- ASF (Formato de Sistemas Avançados), criando no DirectShow
- DirectShow, criando arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e06b6deb6dc9f07115f8143309d32dcf4a58a0f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406179"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Criando arquivos ASF no DirectShow (Windows Media Format SDK 11)

Você pode usar o DirectShow para criar arquivos ASF diretamente de fontes de captura, como gravações DV ou para transcodificar outros arquivos em Windows Media Format. Em qualquer cenário, os aplicativos criam grafos de filtro que incluem o filtro [Wm ASF Writer](wm-asf-writer-filter.md) como o renderdor.

O Wm ASF Writer fornece um wrapper parcial para Windows Media Format SDK. Os aplicativos podem usar a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) do filtro para passar um perfil do sistema (versões 4, 7 ou 8) ou usar o SDK do Windows Media Format diretamente para criar um perfil personalizado para passar para o filtro. Para adicionar metadados e outras informações de header, o aplicativo usa a interface [**IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) que pode ser obtida do filtro. Depois que o perfil e os metadados foram configurados, o aplicativo pode simplesmente executar o grafo de filtro. Internamente, o filtro usa o Windows Media Format SDK para gravar o arquivo. O filtro lida com todos os detalhes de sincronização de áudio e vídeo, que, de outra forma, seriam de responsabilidade do aplicativo.

Esse processo é explicado mais detalhadamente nas seções a seguir.



| Seção                                                                                                           | Descrição                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Configurando o WM ASF Writer (QASF)](configuring-the-wm-asf-writer--qasf.md)                                   | Descreve como configurar o filtro Wm ASF Writer.                                   |
| [Criando grafos de filtro para gravar arquivos ASF (QASF)](building-filter-graphs-to-write-asf-files--qasf.md)           | Descreve como criar grafos de transcodificação e captura de arquivo.                           |
| [Configurando perfis e outras propriedades de arquivo (QASF)](configuring-profiles-and-other-file-properties--qasf.md) | Descreve como executar várias tarefas de configuração de arquivo ASF usando o Wm ASF Writer. |



 

 

 
