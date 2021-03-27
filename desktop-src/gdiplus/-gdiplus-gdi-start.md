---
description: O Windows GDI+ é uma API baseada em classe para programadores C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090330"
---
# <a name="gdi"></a>GDI+

## <a name="purpose"></a>Finalidade

O Windows GDI+ é uma API baseada em classe para programadores C/C++. Ele permite que os aplicativos usem gráficos e texto formatado na tela de vídeo e na impressora. Os aplicativos baseados na API do Microsoft Win32 não acessam o hardware de gráficos diretamente. Em vez disso, a GDI+ interage com drivers de dispositivo em nome dos aplicativos. O GDI+ também tem suporte do Microsoft Win64.

## <a name="where-applicable"></a>Quando aplicável

Não há suporte para funções e classes GDI+ para uso em um serviço do Windows. A tentativa de usar essas funções e classes de um serviço do Windows pode gerar problemas inesperados, como desempenho de serviço reduzido e erros ou exceções de tempo de execução.

> [!Note]  
> Ao usar a API GDI+, você nunca deve permitir que seu aplicativo Baixe fontes arbitrárias de fontes não confiáveis. O sistema operacional requer privilégios elevados para garantir que todas as fontes instaladas sejam confiáveis.

## <a name="developer-audience"></a>Público de desenvolvedores

A interface baseada em classe GDI+ C++ foi projetada para ser usada por programadores C/C++. É necessário ter familiaridade com a interface gráfica do usuário do Windows e com a arquitetura controlada por mensagem.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O GDI+ pode ser usado em todos os aplicativos baseados no Windows. O GDI+ foi introduzido no Windows XP e no Windows Server 2003. Para obter informações sobre quais sistemas operacionais são necessários para usar uma classe ou um método específico, consulte a seção mais informações da documentação para a classe ou o método.

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                    | Descrição                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [Visão geral](-gdiplus-about-gdi--about.md)<br/>     | Informações gerais sobre GDI+.<br/>            |
| [Usando](-gdiplus-using-gdi--use.md)<br/>          | Tarefas e exemplos usando o GDI+.<br/>             |
| [Referência](-gdiplus-class-gdi-reference.md)<br/> | Documentação da API baseada em classe do GDI+ C++.<br/> |

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[GDI do Windows](../gdi/windows-gdi.md)
</dt> <dt>

[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> <dt>

[Aquisição de imagem do Windows](../wia/-wia-startpage.md)
</dt> <dt>

[OpenGL](../opengl/opengl.md)
</dt> <dt>

[Multimídia do Windows](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
