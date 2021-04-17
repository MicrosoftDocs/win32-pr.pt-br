---
title: Serviços de Área de Trabalho Remota interfaces AudioEndpoint
description: As interfaces a seguir são usadas com a API AudioEndpoint.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761324"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Serviços de Área de Trabalho Remota interfaces AudioEndpoint

As interfaces a seguir são usadas com a API AudioEndpoint.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

Inicializa um objeto de ponto de extremidade do dispositivo e obtém os recursos do dispositivo que ele representa.

</dd> <dt>

[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

Fornece informações para o mecanismo de áudio sobre um ponto de extremidade de áudio. Essa interface é implementada por um ponto de extremidade de áudio.

</dd> <dt>

[**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

Controla o estado de fluxo de um ponto de extremidade.

</dd> <dt>

[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Obtém a diferença entre as posições de leitura e gravação atuais no buffer de ponto de extremidade.

</dd> <dt>

[**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

Obtém o buffer de entrada para cada passagem de processamento.

</dd> <dt>

[**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

Obtém o buffer de saída para cada passagem de processamento.

</dd> </dl>

## <a name="remarks"></a>Comentários

O Serviços de Área de Trabalho Remota API AudioEndpoint é para uso em cenários de Área de Trabalho Remota; Não é para aplicativos cliente.

 

 




