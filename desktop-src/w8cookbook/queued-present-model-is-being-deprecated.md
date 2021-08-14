---
title: O modelo presente na fila está sendo preterido
description: O modelo presente na fila está sendo preterido
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cb1d4d07a824c2c6f9d0136259aec98b89c53e1320ceb6402241f881e312fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211341"
---
# <a name="queued-present-model-is-being-deprecated"></a>O modelo presente na fila está sendo preterido

## <a name="platforms"></a>Plataformas

**Clientes** – após Windows 8  
**Servidores** – após Windows Server 2012  


## <a name="description"></a>Descrição

Na versão Windows após Windows 8, essas APIs retornarão E \_ NOTIMPL:

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

Além disso, essa API aceitará apenas o valor NULL para o parâmetro hwnd:

-   DwmGetCompositionTimingInfo

Vamos parar de dar suporte a DwmGetCompositionTimingInfo com hwnd != NULL e remover a funcionalidade associada. Se o valor não NULL para hwnd for especificado, essa API retornará E \_ INVALIDARG.

Também não recomendamos o uso da API DwmGetCompositionTimingInfo e sugerimos que os desenvolvedores alternem para o modelo de incompatibilidade DXGI e a API de estatísticas DX presente associada.

## <a name="manifestation"></a>Manifestação

Os aplicativos que usam o modelo presente na fila não funcionarão corretamente. A manifestação exata depende do aplicativo específico, mas pode variar de tempo de apresentação incorreto até o aplicativo sair inesperadamente). Na prática, não esperamos ver muitos (se algum) aplicativos desse tipo. Esse modelo foi usado pelo player de mídia do Vista, que não será usado no Windows 8 (e, possivelmente, o antigo Zune player). No momento, não temos informações sobre outros aplicativos que realmente usam esse modelo.

## <a name="solution"></a>Solução

Os desenvolvedores precisam usar o modo de apresentação de inatividade DXGI em vez de estar na fila (disponível no runtime DX9 desde o Windows 7 e em runtimes DX10 e DX11 no Windows 8).

## <a name="tests"></a>Testes

Execute testes gerais para garantir que os componentes Windows de entrada e os principais produtos continuem a funcionar na próxima versão do Windows.

 

 




