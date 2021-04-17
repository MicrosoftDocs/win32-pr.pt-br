---
description: Para selecionar uma das NICs registradas no computador local, chame a função GetNPPBlobFromUI.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Selecionando uma NIC registrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759618"
---
# <a name="selecting-a-registered-nic"></a>Selecionando uma NIC registrada

Para selecionar uma das NICs registradas no computador local, chame a função [**GetNPPBlobFromUI**](getnppblobfromui.md) . Essa função usa o Monitor de Rede interface do usuário para exibir as NICs registradas e retorna o BLOB NPP que representa a NIC que você selecionar. Você pode exibir todas as NICs registradas no computador local ou em um conjunto menor de NICs filtradas. Para filtrar as NICs exibidas, forneça um [*blob de filtro*](f.md) quando a chamada for feita.

> [!Note]  
> Quando a função [**GetNPPBlobFromUI**](getnppblobfromui.md) é chamada, o [*localizador de NPP*](n.md) se comunica com as DLLs do NPP para obter as estruturas de blob NPP que representam as NICs registradas. Para obter mais informações e um procedimento sobre como usar a interface do usuário do Monitor de Rede diretamente, consulte o tópico "selecionar uma caixa de diálogo de rede" na ajuda online do Monitor de Rede.

 

Quando você chama a função [**GetNPPBlobFromUI**](getnppblobfromui.md) , a caixa de diálogo **selecionar uma rede** é exibida. A partir dele, você pode exibir os detalhes do NPPs registrados no computador local. Essas informações incluem NPPs local e NPPs remota. Na caixa de diálogo, você pode selecionar uma NIC específica e exibir os detalhes de sua estrutura de BLOB NPP associada.

A ilustração a seguir mostra as configurações típicas de um NPP NDIS fornecido pelo Monitor de Rede.

![configurações típicas de um NPP NDIS fornecido pelo monitor de rede](images/networkdb.png)

A tabela a seguir lista os tópicos que descrevem cada método de seleção de NIC.



| Para obter informações sobre                                                                          | Consulte                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Como especificar um filtro que limita as NICs exibidas na caixa de diálogo **selecionar uma rede** . | [Especificando um BLOB de filtro](specifying-a-filter-blob.md)                                             |
| Como selecionar uma NIC chamando a função [**GetNPPBlobFromUI**](getnppblobfromui.md) .      | [Selecionando uma NIC usando GetNPPBlobFromUI](getnppblobfromui.md)                                       |
| Como selecionar uma NIC de uma tabela de BLOB NPP fornecida.                                            | [Selecionando uma NIC de uma tabela de BLOB NPP fornecida](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



