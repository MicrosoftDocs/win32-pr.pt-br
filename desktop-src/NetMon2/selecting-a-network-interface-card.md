---
description: Monitor de Rede fornece três funções para selecionar uma NIC (placa de interface de rede). Essas funções fornecem três maneiras de enumerar um conjunto de NICs e selecionar aquela que você deseja usar. A tabela a seguir lista essas funções.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Selecionando uma placa de interface de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f93341bb169f2672579ac6764186925b7190f1ac52c698e2426e1c20d3e854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074486"
---
# <a name="selecting-a-network-interface-card"></a>Selecionando uma placa de interface de rede

Monitor de Rede fornece três funções para selecionar uma NIC (placa de interface de rede). Essas funções fornecem três maneiras de enumerar um conjunto de NICs e selecionar aquela que você deseja usar. A tabela a seguir lista essas funções.



| Função                                                 | Descrição                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | Usa a Monitor de Rede interface do usuário para exibir as NICs registradas e retorna o BLOB do NPP que representa a NIC em que você está interessado.           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | Retorna uma tabela BLOB. O aplicativo deve enumerar a tabela e selecionar um BLOB NPP.                                                       |
| [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) | Usa a interface Monitor de Rede para exibir os BLOBs NPP fornecidos e retorna o BLOB NPP que representa a NIC em que você está interessado. |



 

Cada NIC é representada por um BLOB (objeto binário grande) NPP. Essas funções podem retornar um único BLOB NPP daqueles registrados no computador, um único BLOB NPP de uma tabela de BLOB NPP fornecida ou uma tabela de BLOBs NPP que o chamador deve usar para selecionar um BLOB específico. Nos dois primeiros casos, ao selecionar entre as NICs registradas ou em uma tabela de BLOB NPP fornecida, a interface do usuário Monitor de Rede exibe as NICs que você pode selecionar.

> [!Note]  
> Monitor de Rede usa um recurso chamado Localizador NPP para enumerar as NICs registradas no computador local. O NPP Finder é um componente Npptools.dll.

 



| Para obter informações sobre                            | Consulte                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Selecionando uma NIC registrada no computador local | [Selecionando uma NIC registrada](selecting-a-registered-nic.md)                                         |
| Selecionando uma NIC de uma tabela de BLOB NPP fornecida   | [Selecionando uma NIC em uma tabela de BLOB NPP fornecida](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Recuperando uma tabela de BLOB NPP                     | [Selecionando uma NIC em uma tabela de BLOB NPP retornada](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



