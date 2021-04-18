---
title: Interfaces da camada de depuração
description: As interfaces a seguir são declaradas em d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2020
ms.locfileid: "105752612"
---
# <a name="debug-layer-interfaces"></a>Interfaces de camada de depuração

As interfaces a seguir são definidas em `d3d12sdklayers.h` .

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**ID3D12Debug**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Uma interface de depuração controla as configurações de depuração e valida o estado do pipeline. Ele só poderá ser usado se a camada de depuração estiver ativada. |
| [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Adiciona a validação baseada em GPU e a sincronização de fila de comando dependente à camada de depuração. |
| [**ID3D12Debug2**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Adiciona níveis configuráveis de validação de GPU-Based. |
| [**ID3D12Debug3**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Adiciona à validação baseada em GPU da camada de depuração, à sincronização da fila de comandos dependentes e aos níveis configuráveis da validação baseada em GPU. |
| [**ID3D12DebugCommandList**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Fornece métodos para monitorar e depurar uma lista de comandos. |
| [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Essa interface permite a modificação de configurações adicionais da camada de depuração da lista de comandos. |
| [**ID3D12DebugCommandQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Fornece métodos para monitorar e depurar uma fila de comando. |
| [**ID3D12DebugDevice**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Essa interface representa um dispositivo de gráficos para depuração. |
| [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Especifica as configurações da camada de depuração de todo o dispositivo. |
| [**ID3D12InfoQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Uma interface de fila de informações armazena, recupera e filtra mensagens de depuração. A fila consiste em uma fila de mensagens, uma pilha de filtro de armazenamento opcional e uma pilha de filtro de recuperação opcional. |
| [**ID3D12SharingContract**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Parte de um contrato entre camadas de diagnóstico D3D11On12 e ferramentas de diagnóstico de gráficos. |

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configuração do ambiente programação do Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referência da camada de depuração](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> </dl>