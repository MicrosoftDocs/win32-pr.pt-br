---
description: Monitor de Rede fornece três funções para selecionar uma placa de interface de rede (NIC). Essas funções fornecem três maneiras de enumerar um conjunto de NICs e selecionar aquela que você deseja usar. A tabela a seguir lista essas funções.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Selecionando uma placa de interface de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091392"
---
# <a name="selecting-a-network-interface-card"></a>Selecionando uma placa de interface de rede

Monitor de Rede fornece três funções para selecionar uma placa de interface de rede (NIC). Essas funções fornecem três maneiras de enumerar um conjunto de NICs e selecionar aquela que você deseja usar. A tabela a seguir lista essas funções.



| Função                                                 | Descrição                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | Usa o Monitor de Rede interface do usuário para exibir as NICs registradas e retorna o BLOB NPP que representa a NIC em que você está interessado.           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | Retorna uma tabela de BLOB. O aplicativo deve enumerar a tabela e selecionar um BLOB NPP.                                                       |
| [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) | Usa a interface Monitor de Rede para exibir os BLOBs NPP fornecidos e retorna o BLOB NPP que representa a NIC em que você está interessado. |



 

Cada NIC é representada por um BLOB (objeto binário grande) NPP. Essas funções podem retornar um único BLOB NPP dos registrados no computador, um único BLOB de NPP de uma tabela de BLOB NPP fornecida ou uma tabela de BLOBs NPP que o chamador deve usar para selecionar um BLOB específico. Nos dois primeiros casos, ao selecionar as NICs registradas ou de uma tabela de BLOB NPP fornecida, a interface do usuário do Monitor de Rede exibe as NICs que você pode selecionar.

> [!Note]  
> Monitor de Rede usa um recurso chamado NPP Finder para enumerar as NICs registradas no computador local. O NPP Finder é um componente do Npptools.dll.

 



| Para obter informações sobre                            | Consulte                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Selecionando uma NIC registrada no computador local | [Selecionando uma NIC registrada](selecting-a-registered-nic.md)                                         |
| Selecionando uma NIC de uma tabela de BLOB NPP fornecida   | [Selecionando uma NIC de uma tabela de BLOB NPP fornecida](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Recuperando uma tabela de BLOB NPP                     | [Selecionando uma NIC de uma tabela de BLOB NPP retornada](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



