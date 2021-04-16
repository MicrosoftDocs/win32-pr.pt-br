---
title: O modelo presente na fila está sendo preterido
description: O modelo presente na fila está sendo preterido
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "105765617"
---
# <a name="queued-present-model-is-being-deprecated"></a>O modelo presente na fila está sendo preterido

## <a name="platforms"></a>Plataformas

**Clientes** – após o Windows 8  
**Servidores** – após o Windows Server 2012  


## <a name="description"></a>Descrição

Na versão do Windows após o Windows 8, essas APIs retornarão E \_ NOTIMPL:

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

Além disso, essa API só aceitará o valor nulo para o parâmetro hWnd:

-   DwmGetCompositionTimingInfo

Vamos parar de dar suporte a DwmGetCompositionTimingInfo com HWND! = NULL e remover a funcionalidade associada. Se um valor não nulo para HWND for especificado, essa API retornará E \_ INVALIDARG.

Também desencorajamos o uso da API DwmGetCompositionTimingInfo e sugerem que os desenvolvedores alternem para o modelo de flip-DXGI e a API de estatísticas do DX presente associado.

## <a name="manifestation"></a>Manifestação

Os aplicativos que usam o modelo em fila no momento não funcionarão corretamente. A manifestação exata depende do aplicativo específico, mas pode variar de tempo de apresentação incorreto para o aplicativo que está saindo inesperadamente). Na prática, não esperamos ver muitos aplicativos (se houver) tais. Esse modelo foi usado pelo Media Player do vista, que não será usado no Windows 8 (e possivelmente no antigo Zune Player). Neste momento, não temos informações sobre outros aplicativos que realmente usam esse modelo.

## <a name="solution"></a>Solução

Os desenvolvedores precisam usar o modo de apresentação de flip-DXGI em vez de estar na fila presente (disponível no tempo de execução do DX9 desde o Windows 7 e em tempos de execução DX10 e DX11 no Windows 8).

## <a name="tests"></a>Testes

Execute testes gerais para garantir que os componentes do Windows da caixa de entrada e os principais produtos continuem a funcionar na próxima versão do Windows.

 

 




