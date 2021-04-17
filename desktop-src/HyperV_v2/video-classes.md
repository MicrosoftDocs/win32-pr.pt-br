---
description: Todas as máquinas virtuais refletem a presença de um controlador de vídeo S3 emulado e um controlador de vídeo mais rápido e sintético.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Classes de vídeo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461303"
---
# <a name="video-classes"></a>Classes de vídeo

Todas as máquinas virtuais refletem a presença de um controlador de vídeo S3 emulado e um controlador de vídeo mais rápido e sintético.

Cada controlador de vídeo tem um objeto de cabeçalho de vídeo associado a ele. Somente um controlador de vídeo pode estar ativo em uma máquina virtual a qualquer momento.

Uma conexão de terminal está presente para cada sessão remota ativa conectada a uma máquina virtual.

Veja a seguir as classes WMI de virtualização relacionadas ao vídeo.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                  | Descrição                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ S3DisplayController**](msvm-s3displaycontroller.md)<br/>               | Representa o estado do controlador S3 emulado que está presente em cada configuração de máquina virtual.<br/>       |
| [**Msvm \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)<br/> | Representa o estado do controlador de vídeo sintético que está presente em cada configuração de máquina virtual.<br/> |
| [**Msvm \_ SystemTerminalConnection**](msvm-systemterminalconnection.md)<br/>     | Associa uma máquina virtual a uma conexão de terminal.<br/>                                                        |
| [**Msvm \_ TerminalConnection**](msvm-terminalconnection.md)<br/>                 | Indica o estado de uma sessão remota ativa que interage com uma máquina virtual.<br/>                             |
| [**Msvm \_ VideoHead**](msvm-videohead.md)<br/>                                   | Descreve a superfície de desenho primária em um controlador de vídeo.<br/>                                                  |
| [**Msvm \_ VideoHeadOnController**](msvm-videoheadoncontroller.md)<br/>           | Associa uma cabeça de vídeo com o controlador de vídeo que a inclui.<br/>                                             |



 

 

 




