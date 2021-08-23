---
description: Ao selecionar uma NIC (placa de interface de rede) registrada listada em um computador local, você pode usar um BLOB de filtro para desconsiderar as NICs nas quais você não está interessado.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Especificando um BLOB de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486a5dfe318da50a921560c92b82a3a3bf05a9434a4ac609b7f135afd7bf5a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555346"
---
# <a name="specifying-a-filter-blob"></a>Especificando um BLOB de filtro

Ao selecionar uma NIC (placa de interface de rede) registrada listada em um computador local, você pode usar um [*blob de filtro*](f.md) para desconsiderar as NICs nas quais você não está interessado. Por exemplo, você pode restringir a pesquisa de um tipo específico de cartão (como ETHERNET) ou um endereço MAC específico.

Durante a pesquisa de uma NIC, cada entrada no BLOB de filtro deve corresponder a uma entrada equivalente no BLOB NPP que representa a NIC. Os BLOBs de filtro também podem ser [*BLOBs especiais*](s.md).

Quando a função [**GetNPPBlobFromUI**](getnppblobfromui.md) é chamada, o blob de filtro restringe as NICs exibidas na caixa de diálogo **selecionar uma rede** . Quando a função [**GetNPPBlobTable**](getnppblobtable.md) é chamada, o blob de filtro restringe as NICs retornadas na tabela de BLOB.

Para usar o filtro, você deve criar um BLOB de filtro, definir os valores das propriedades que você deseja filtrar (incluindo quaisquer entradas de BLOB especiais) e, em seguida, especificar o filtro de BLOB e uma chamada para a função [**GetNPPBlobTable**](getnppblobtable.md) ou [**GetNPPBlobFromUI**](getnppblobfromui.md) .



| Para obter informações sobre                                 | Consulte                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Como selecionar uma NIC registrada em um computador local | [Selecionando uma NIC registrada](selecting-a-registered-nic.md)                                         |
| Recuperando uma tabela de BLOB NPP                       | [Selecionando uma NIC de uma tabela de BLOB NPP retornada](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



