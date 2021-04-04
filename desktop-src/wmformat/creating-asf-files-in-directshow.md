---
title: Criando arquivos ASF no DirectShow (SDK do Windows Media Format 11)
description: Criando arquivos ASF no DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- SDK do Windows Media Format, criando arquivos ASF no DirectShow
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), criando no DirectShow
- ASF (formato de sistemas avançados), criando no DirectShow
- DirectShow, criando arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085055"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Criando arquivos ASF no DirectShow (SDK do Windows Media Format 11)

Você pode usar o DirectShow para criar arquivos ASF diretamente de fontes de captura, como camcorders DV, ou para transcodificar outros arquivos no formato de mídia do Windows. Em qualquer cenário, os aplicativos criam gráficos de filtro que incluem o filtro de [gravador ASF do WM](wm-asf-writer-filter.md) como o renderizador.

O gravador ASF do WM fornece um wrapper parcial para o SDK do Windows Media Format. Os aplicativos podem usar a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) do filtro para passar um perfil do sistema (versões 4, 7 ou 8) ou usar o SDK do Windows Media Format diretamente para criar um perfil personalizado para passar para o filtro. Para adicionar metadados e outras informações de cabeçalho, o aplicativo usa a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , que pode ser obtida no filtro. Depois que o perfil e os metadados tiverem sido configurados, o aplicativo poderá simplesmente executar o gráfico de filtro. Internamente, o filtro usa o Windows Media Format SDK para gravar o arquivo. O filtro manipula todos os detalhes de sincronização de áudio e vídeo, que de outra forma seria a responsabilidade do aplicativo.

Esse processo é explicado com mais detalhes nas seções a seguir.



| Seção                                                                                                           | Descrição                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Configurando o gravador ASF do WM (QASF)](configuring-the-wm-asf-writer--qasf.md)                                   | Descreve como configurar o filtro do gravador ASF do WM.                                   |
| [Criando gráficos de filtro para gravar arquivos ASF (QASF)](building-filter-graphs-to-write-asf-files--qasf.md)           | Descreve como criar gráficos de transcodificação e captura de arquivos.                           |
| [Configurando perfis e outras propriedades de arquivo (QASF)](configuring-profiles-and-other-file-properties--qasf.md) | Descreve como executar várias tarefas de configuração de arquivo ASF usando o gravador ASF do WM. |



 

 

 
