---
title: Interfaces da camada de depuração
description: As interfaces a seguir são declaradas em d3d12sdklayers.h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7e16d6c593f2dcfcc46266102ac15a61386ef
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812875"
---
# <a name="debug-layer-interfaces"></a>Interfaces de camada de depuração

As interfaces a seguir são definidas em `d3d12sdklayers.h` .

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**ID3D12Debug**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Uma interface de depuração controla as configurações de depuração e valida o estado do pipeline. Ele só poderá ser usado se a camada de depuração estiver ativa. |
| [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Adiciona validação baseada em GPU e Sincronização de Fila de Comandos Dependentes à camada de depuração. |
| [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Adiciona níveis configuráveis de GPU-Based Validação. |
| [**ID3D12Debug3**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Adiciona à validação baseada em GPU da camada de depuração, à Sincronização de Fila de Comandos Dependentes e aos níveis configuráveis de validação baseada em GPU. |
| [**ID3D12Debug4**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug4) | Adiciona a capacidade de desabilitar a camada de depuração. |
| [**ID3D12Debug5**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug5) | Adiciona à camada de depuração a capacidade de configurar a nomeação automática de objetos. |
| [**ID3D12DebugCommandList**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Fornece métodos para monitorar e depurar uma lista de comandos. |
| [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Essa interface permite a modificação de configurações adicionais da camada de depuração da lista de comandos. |
| [**ID3D12DebugCommandQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Fornece métodos para monitorar e depurar uma fila de comandos. |
| [**ID3D12DebugDevice**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Essa interface representa um dispositivo gráfico para depuração. |
| [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Especifica as configurações da camada de depuração em todo o dispositivo. |
| [**ID3D12InfoQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Uma interface de fila de informações armazena, recupera e filtra mensagens de depuração. A fila consiste em uma fila de mensagens, uma pilha de filtros de armazenamento opcional e uma pilha de filtros de recuperação opcional. |
| [**ID3D12SharingContract**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Parte de um contrato entre as camadas de diagnóstico D3D11On12 e as ferramentas de diagnóstico de gráficos. |

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configuração do ambiente programação do Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referência da camada de depuração](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> </dl>