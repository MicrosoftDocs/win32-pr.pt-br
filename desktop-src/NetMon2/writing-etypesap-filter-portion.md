---
description: A parte ETYPE/SAP do filtro de captura notifica o driver de Monitor de Rede para aceitar quadros que têm uma combinação específica de ETYPEs e SAPs (pontos de acesso de serviço).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Gravando a parte do filtro ETYPE/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922322"
---
# <a name="writing-etypesap-filter-portion"></a>Gravando a parte do filtro ETYPE/SAP

A parte ETYPE/SAP do filtro de captura notifica o driver de Monitor de Rede para aceitar quadros que têm uma combinação específica de ETYPEs e SAPS ( [*pontos de acesso de serviço*](s.md) ). Os ETYPEs e SAPs são maneiras de os protocolos de nível inferior, como Ethernet, LLC e snap, indicam qual protocolo os segue. Especificamente:

-   Ethernet especifica um ETYPE
-   O LLC especifica um SAP
-   Snap especifica um ETYPE

## <a name="etypesap-capture-filter-flags"></a>Sinalizadores de filtro de captura de ETYPE/SAP

Use as informações a seguir para definir os sinalizadores no membro **FilterFlags** da estrutura [**CAPTUREFILTER**](capturefilter.md) .



| Sinalizador                                         | Significado                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_os sinalizadores CAPTUREFILTER \_ incluem \_ todos os \_ SAPs   | Passa todos os valores SAP e notifica o driver de que todos os valores SAP são válidos. Se combinado com quaisquer valores no membro **lpSapTable** , esse sinalizador notificará o driver de que todos os valores SAP, exceto aqueles no **lpSapTable** , são válidos.<br/>           |
| \_os sinalizadores CAPTUREFILTER \_ incluem \_ todos os \_ ETYPES | Passa todos os valores de ETYPE e notifica o driver de que todos os valores de ETYPE são válidos. Se combinado com quaisquer valores no membro **lpEtypeTable** , esse sinalizador notificará o driver de que todos os valores de ETYPE, exceto aqueles no **lpEtypeTable** , são válidos.<br/> |
| CAPTUREFILTER \_ sinalizadores \_ \_ somente locais           | A definição desse sinalizador não definirá uma NIC para o modo P. Você verá apenas o tráfego local (todos os quadros no computador local).                                                                                                                                          |
| CAPTUREFILTER \_ sinalizadores de \_ manutenção \_ brutos             | Mantém os quadros MAC SMT e token ring.                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a>Configurações do filtro de captura do ETYPE/SAP

Use as informações a seguir para definir os membros **lpSapTable** e **LpEtypeTable** da estrutura [**CAPTUREFILTER**](capturefilter.md) .



| Configuração          | Significado                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lpSapTable**   | Lista os valores SAP que você deseja que o driver passe. Essa lista informa o driver de Monitor de Rede para validar qualquer quadro que contenha uma correspondência. Se CAPTUREFILTER \_ flags \_ incluir \_ todos os \_ SAPs for definido, isso se tornará uma lista de exceção (se for encontrada, não passará).           |
| **lpEtypeTable** | Lista os valores de ETYPE que você deseja que o driver de Monitor de Rede passe. Essa lista só informa ao driver para validar qualquer quadro que contenha uma correspondência. Se \_ os sinalizadores CAPTUREFILTERs \_ incluírem \_ todos os \_ ETYPES forem definidos, isso se tornará uma lista de exceção (se for encontrada, não passará). |



 

 

 




