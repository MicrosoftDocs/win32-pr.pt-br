---
description: Determine a versão do WUA (agente de Windows Update) antes de usá-lo.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Determinando a versão atual do WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d8e013f4e8189c71b9e4510fdaebcdf1e2f749e3d8dfffd6256128e214ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049494"
---
# <a name="determining-the-current-version-of-wua"></a>Determinando a versão atual do WUA

para obter informações gerais sobre como atualizar o WUA, incluindo instruções passo a passo para determinar programaticamente de dentro de seu aplicativo se a versão do WUA em execução no computador atende às suas necessidades, consulte [atualizando o agente de Windows Update](updating-the-windows-update-agent.md).

nas versões do Windows anteriores ao Windows 7 e Windows Server 2008 R2, você deve determinar a versão instalada do WUA (agente de Windows Update) antes de usá-lo. a versão atual do WUA é determinada pela versão do Wuaueng.dll que está em execução no \\ subdiretório System32 da instalação atual do Windows. Se a versão do Wuaueng.dll for a versão 5.4.3790.1000 ou posterior, o WUA será instalado. Uma versão anterior a 5.4.3790.1000 indica que o SUS (Software Update Services) 1,0 está instalado.

Quando é feita uma chamada ao SUS 1,0 usando a API do WUA, um **HRESULT** de Wu \_ E \_ au \_ LEGACYSERVER é retornado.

Você também pode usar o método [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) para recuperar a versão atual do arquivo do Wuapi.dll que está sendo executado em um computador. Não há suporte para a interface [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) no WUA 1,0.
