---
description: Controles de reprodução no TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Controles de reprodução no TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550441"
---
# <a name="playback-controls-in-topoedit"></a>Controles de reprodução no TopoEdit

Depois que uma topologia é resolvida, ela é enfileirada na sessão de mídia para reprodução. O TopoEdit fornece controle de transporte para alterar o estado da topologia na sessão de mídia.

A tabela a seguir mostra o comando de menu/barra de ferramentas e o método equivalente Media Foundation para cada operação.



| Comando de menu/barra de ferramentas                                                                                                                                                                                                                          | Método de Media Foundation                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| No menu **controles** , clique em **reproduzir**. \[ nova linha \] ou \[ nova linha \] clique no botão **reproduzir** na barra de ferramentas (mostrada na imagem a seguir). \[ \] ![ captura de tela de nova linha do botão de reprodução](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**IMFMediaSession:: iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| No menu **controles** , clique em **parar**. \[ nova linha \] ou \[ nova linha \] clique no botão **parar** na barra de ferramentas (mostrada na imagem a seguir). \[ \] ![ captura de tela de nova linha do botão parar](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| No menu **controles** , clique em **Pausar**. \[ nova linha \] , ou \[ nova linha, \] clique no botão **Pausar** na barra de ferramentas (mostrada na imagem a seguir). \[ \] ![ captura de tela de nova linha do botão Pausar](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Para obter informações sobre como controlar a reprodução programaticamente usando APIs Media Foundation, consulte [como controlar os Estados de apresentação](how-to-control-presentation-states.md).

## <a name="seeking"></a>Atingir

Se a topologia for pesquisável, você poderá buscar usando a barra de busca (mostrada na imagem a seguir) para especificar um local na linha do tempo da topologia para começar a reprodução.

![captura de tela da barra de busca](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Se a origem da mídia for pesquisável, o comando Stop também buscará a topologia de volta ao início do fluxo.

 

## <a name="changing-the-playback-rate"></a>Alterando a taxa de reprodução

Se a fonte de mídia subjacente para a topologia oferecer suporte a várias taxas de reprodução, você poderá usar a barra de taxa para alterar a taxa de reprodução. Para avançar rapidamente uma topologia na sessão de mídia, aumente a taxa arrastando o controle deslizante para a direita, conforme mostrado na imagem a seguir.

![captura de tela da barra de taxas](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> Nesta versão, o TopoEdit dá suporte apenas a tarifas positivas. Não há suporte para reprodução reversa.

 

Para obter informações sobre como alterar a taxa de reprodução programaticamente usando APIs Media Foundation, consulte [sobre o controle de taxa](about-rate-control.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TopoEdit menus](topoedit-menus.md)
</dt> <dt>

[Barra de ferramentas TopoEdit](topoedit-toolbar.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



