---
description: O Monitor de Rede usa três tipos de BLOBs (objetos binários grandes) para selecionar e conectar placas de interface de rede (NICs), capturar dados e manipular dados de NPP.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Tipos de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171822"
---
# <a name="blob-types"></a>Tipos de BLOB

O Monitor de Rede usa três tipos de BLOBs (objetos binários grandes) para selecionar e conectar placas de interface de rede (NICs), capturar dados e manipular dados de NPP.

## <a name="npp-blob"></a>BLOB NPP

Os aplicativos usam BLOBs NPP para se conectar a uma NIC específica por meio de um NPP. (O aplicativo faz a conexão com uma chamada para **CreateNPPInterface** e dados de localização no blob NPP.) Um aplicativo também pode armazenar seus dados de configuração no BLOB NPP para configurar o NPP. Além disso, um aplicativo que salva seu BLOB NPP não é necessário para percorrer o localizador para reutilizar esse BLOB.

## <a name="filter-blob"></a>BLOB de filtro

Um BLOB de filtro contém critérios definidos pelo aplicativo que você pode usar para selecionar um NPP e uma NIC. Por exemplo, um aplicativo pode solicitar uma NIC específica, somente placas Ethernet ou cartões que dão suporte a uma taxa de captura de quadro específica.

## <a name="special-blob"></a>BLOB especial

Quando um NPP requer dados adicionais antes de poder retornar um BLOB NPP a um aplicativo, o NPP usa um BLOB especial. Geralmente, o aplicativo não precisará ou usará BLOBs especiais para que eles não sejam retornados a um aplicativo, a menos que um sinalizador específico seja definido em uma chamada de função. Por exemplo, um NPP remoto usa um BLOB especial porque um nome de caminho é necessário para estabelecer uma conexão. Um aplicativo que recebe um BLOB especial de NPP remoto pode adicionar a cadeia de caracteres e chamar de volta para o localizador para obter uma tabela de BLOB NPP. Para obter mais informações, consulte [entradas de blob especiais](special-blob-entries.md).

 

 



