---
description: Controles de reprodução no TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controles de reprodução no TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c59dfceb30f839ba58d37385a3178d42429eb858c98f3f5196dd95141ac2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239662"
---
# <a name="playback-controls-in-topoedit"></a>Controles de reprodução no TopoEdit

Depois que uma topologia é resolvida, ela é en fila na Sessão de Mídia para reprodução. TopEdit fornece controle de transporte para alterar o estado da topologia na Sessão de Mídia.

A tabela a seguir mostra o comando menu/barra de ferramentas e o método Media Foundation equivalente para cada operação.



| Comando Menu/Barra de Ferramentas                                                                                                                                                                                                                          | Media Foundation método                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| No menu **Controles,** clique em **Reproduzir**. \[ newline -or- newline clique no botão reproduzir na barra de \] \[ ferramentas \] (mostrado na imagem a seguir).  \[ captura de \] ![ tela de nova linha do botão reproduzir](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| No menu **Controles,** clique em **Parar**. \[ newline \] -or- newline clique no botão Parar na barra de \[ ferramentas \] (mostrado na imagem a seguir).  \[ captura de \] ![ tela de nova linha do botão Parar](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| No menu **Controles,** clique em **Pausar**. \[ newline \] -or- \[ newline clique no botão \] **pausar** na barra de ferramentas (mostrado na imagem a seguir). \[ captura de \] ![ tela de nova linha do botão pausar](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Para obter informações sobre como controlar a reprodução programaticamente usando APIs Media Foundation, consulte [How to Control Presentation States](how-to-control-presentation-states.md).

## <a name="seeking"></a>Procurando

Se a topologia for buscada, você poderá procurar usando a barra de busca (mostrada na imagem a seguir) para especificar um local na linha do tempo da topologia para iniciar a reprodução.

![captura de tela da barra de busca](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Se a fonte de mídia for buscada, o comando Parar também buscará a topologia de volta para o início do fluxo.

 

## <a name="changing-the-playback-rate"></a>Alterando a taxa de reprodução

Se a fonte de mídia subjacente para a topologia for compatível com várias taxas de reprodução, você poderá usar a barra de taxas para alterar a taxa de reprodução. Para avançar rapidamente uma topologia na Sessão de Mídia, aumente a taxa arrastando o controle deslizante para a direita, conforme mostrado na imagem a seguir.

![captura de tela da barra de taxa](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> Nesta versão, o TopoEdit dá suporte apenas a taxas positivas. Não há suporte para reprodução inversa.

 

Para obter informações sobre como alterar a taxa de reprodução programaticamente usando APIs Media Foundation, consulte [Sobre o Controle de Taxa](about-rate-control.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Menus TopEdit](topoedit-menus.md)
</dt> <dt>

[Barra de ferramentas TopEdit](topoedit-toolbar.md)
</dt> <dt>

[TopEdit](topoedit.md)
</dt> </dl>

 

 



