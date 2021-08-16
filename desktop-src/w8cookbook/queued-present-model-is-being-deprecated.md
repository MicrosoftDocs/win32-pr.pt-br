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

na versão Windows após Windows 8, essas APIs retornarão E \_ NOTIMPL:

-   DwmSetPresentParameters
-   DwmSetDxFrameDuration
-   DwmModifyPreviousDxFrameDuration

Além disso, essa API só aceitará o valor nulo para o parâmetro hWnd:

-   DwmGetCompositionTimingInfo

Vamos parar de dar suporte a DwmGetCompositionTimingInfo com HWND! = NULL e remover a funcionalidade associada. Se um valor não nulo para HWND for especificado, essa API retornará E \_ INVALIDARG.

Também desencorajamos o uso da API DwmGetCompositionTimingInfo e sugerem que os desenvolvedores alternem para o modelo de flip-DXGI e a API de estatísticas do DX presente associado.

## <a name="manifestation"></a>Manifestação

Os aplicativos que usam o modelo em fila no momento não funcionarão corretamente. A manifestação exata depende do aplicativo específico, mas pode variar de tempo de apresentação incorreto para o aplicativo que está saindo inesperadamente). Na prática, não esperamos ver muitos aplicativos (se houver) tais. esse modelo foi usado pelo media player do Vista, que não será usado em Windows 8 (e possivelmente o antigo Zune player). Neste momento, não temos informações sobre outros aplicativos que realmente usam esse modelo.

## <a name="solution"></a>Solução

os desenvolvedores precisam usar o modo de apresentação de flip DXGI em vez de estar na fila presente (disponível no DX9 runtime desde Windows 7 e em tempos de execução DX10 e DX11 no Windows 8).

## <a name="tests"></a>Testes

execute testes gerais para garantir que a caixa de entrada Windows componentes e os principais produtos continuem a funcionar na próxima versão do Windows.

 

 




