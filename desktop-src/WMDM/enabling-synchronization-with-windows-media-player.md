---
title: Habilitando a sincronização com o Windows Media Player
description: Habilitando a sincronização com o Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Gerenciador de Dispositivos, sincronização com o Windows Media Player
- Gerenciador de Dispositivos, sincronização com o Windows Media Player
- Guia de programação, sincronização com o Windows Media Player
- provedores de serviços, sincronização com o Windows Media Player
- criando provedores de serviços, sincronização com o Windows Media Player
- sincronização com o Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770537"
---
# <a name="enabling-synchronization-with-windows-media-player"></a>Habilitando a sincronização com o Windows Media Player

Você pode habilitar um dispositivo para participar da sincronização automática com o Windows Media Player. A sincronização automática significa que, quando um dispositivo sincronizado designado pelo usuário se conectar ao computador, o Windows Media Player baixará, atualizará ou excluirá automaticamente arquivos do dispositivo sem a necessidade de nenhuma entrada adicional do usuário.

Por padrão, os seguintes dispositivos são sincronizados com o Windows Media Player:

-   Dispositivos MTP
-   Dispositivos de armazenamento em massa
-   Dispositivos Windows CE (Windows Media Player 10 Mobile e posterior)

Para que qualquer outro dispositivo seja sincronizado com o Windows Media Player, os seguintes requisitos devem ser atendidos:

-   O dispositivo deve anunciar uma interface de dispositivo PAP que é {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}
-   Os objetos de dispositivo retornados pelo provedor de serviços devem oferecer suporte à interface **IMDSPDevice3** .
-   O parâmetro de dispositivo UseExtendedWmdm deve ser definido como um valor **DWORD** de 1. Consulte [parâmetros do dispositivo](device-parameters.md) para obter mais informações.
-   O provedor de serviços deve implementar as seguintes interfaces:

    [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> <dt>

[**Parâmetros do dispositivo**](device-parameters.md)
</dt> </dl>

 

 




