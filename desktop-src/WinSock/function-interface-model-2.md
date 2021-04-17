---
description: O transporte e o namespace do Windows Sockets&\# 8211; os provedores de serviço são DLLs com um único ponto de entrada de procedimento exportado para a função de inicialização WSPStartup ou NSPStartup do provedor de serviço, respectivamente.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modelo de interface de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813714"
---
# <a name="function-interface-model"></a>Modelo de interface de função

O transporte e o namespace do Windows Sockets – provedores de serviço são DLLs com um único ponto de entrada de procedimento exportado para a função de inicialização [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) ou [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)do provedor de serviço, respectivamente. Todas as outras funções de provedor de serviço tornam-se acessíveis para o \_32.dll Ws2 por meio da tabela de expedição do provedor de serviços. As DLLs do provedor de serviços são carregadas na memória pelo Ws2 \_32.dll somente quando necessário e são descarregadas quando seus serviços não são mais necessários.

O SPI também define várias circunstâncias nas quais um provedor de serviço de transporte chama o \_32.dll Ws2 (upchamadas) para obter os serviços de suporte de dll. A DLL do provedor de serviço de transporte recebe a tabela de expedição de chamada de ws2 \_32.dll por meio do parâmetro *UpcallTable* para [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).

Os provedores de serviços devem ter sua extensão de nome de arquivo alterada de "DLL" para ". WSP "ou". NSP ". Esse requisito não é estrito. Um provedor de serviço ainda funcionará com o \_32.dll Ws2 com qualquer extensão de nome de arquivo.

A SPI do Winsock usa a seguinte convenção de nomenclatura de prefixo de função:

| Prefixo | Significado                          | Descrição                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Provedor de serviços do Windows Sockets | Pontos de entrada do provedor de serviço de transporte           |
| WPU    | Upchamada do provedor do Windows Sockets  | Ws2 \_ pontos de entrada de32.dll para provedores de serviço    |
| WSC    | Configuração do Windows Sockets    | WS2 \_ pontos de entrada de32.dll para miniaplicativos de instalação |
| NSP    | Provedor de namespace               | Pontos de entrada do provedor de namespace                   |



 

Conforme descrito acima, esses pontos de entrada não são exportados (com exceção de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) e [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), mas são acessados por meio de uma troca de tabelas de expedição.

 

 



