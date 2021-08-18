---
description: Se você fornecer contadores em um computador de 64 bits, deverá instalar a versão de 32 bits e de 64 bits do seu provedor no computador se quiser dar suporte a consumidores de 32 e de 64 bits.
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: Suporte de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9756a6eaf95097c881368bc3f150422f494dac04e503da5060f27355827a653c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011424"
---
# <a name="64-bit-support"></a>Suporte de 64 bits

Uma DLL de provedor de dados de desempenho de 64 bits não pode ser executada em um processo de consumidor de 32 bits e uma DLL de provedor de dados de desempenho de 32 bits não pode ser executada em um processo de 64 bits. O registro do provedor só dá suporte a um único `Library` valor para o caminho para a DLL do provedor de dados de desempenho, de modo que você não pode fornecer caminhos diferentes para serem usados por consumidores de 32 bits e consumidores de 64 bits.

As seguintes opções estão disponíveis para dar suporte a provedores v1 em sistemas operacionais de 64 bits:

- **Recomendado:** Instale e registre o caminho para a versão de 32 bits do seu provedor DLL.
  - os consumidores de 32 bits funcionarão nativamente: eles carregarão sua DLL de provedor de 32 bits no processo de consumidor de 32 bits.
  - os consumidores de 64 bits funcionarão indiretamente: eles não poderão carregar sua DLL de provedor de 32 bits no processo de consumidor de 64 bits, mas Windows fará automaticamente o fallback para criar um processo perfhost de 32 bits, carregando sua DLL de provedor de bits de 32 no processo perfhost e enviando dados de desempenho do processo perfhost de 32 bits para o processo consumidor de 64 bits.
- **somente 64 bits:** Instale e registre o caminho para a versão de 64 bits do seu provedor DLL.
  - os consumidores de 32 bits falharão: eles não poderão carregar sua DLL de provedor de 64 bits no processo de 32 bits.
  - os consumidores de 64 bits funcionarão nativamente: eles carregarão sua DLL de provedor de 32 bits em processo.

> [!NOTE]
> vários provedores internos de dados de desempenho Windows instalam uma dll de 32 bits no `%systemroot%\syswow64` , instalam uma dll de 64 bits no `%systemroot%\system32` e registram o `Library` caminho como `%systemroot%\system32\ProviderName.dll` , permitindo que o redirecionamento do sistema de arquivos resolva o caminho para a DLL apropriada. isso tem suporte apenas para provedores de dados de desempenho que fazem parte do sistema operacional Windows. provedores que não fazem parte do sistema operacional Windows não devem instalar arquivos na `Windows` pasta. Os arquivos não reconhecidos na `Windows` pasta podem ser removidos durante a manutenção ou a atualização.
