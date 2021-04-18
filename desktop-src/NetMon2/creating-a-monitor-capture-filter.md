---
description: A criação de um filtro de captura que funciona com Monitor de Rede é um processo de cinco etapas.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Criando um filtro de captura de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785404"
---
# <a name="creating-a-monitor-capture-filter"></a>Criando um filtro de captura de monitor

A criação de um filtro de captura que funciona com o Monitor de Rede é um processo de cinco etapas:

-   [Configurando o filtro ETYPE ou SAP](writing-etypesap-filter-portion.md)
-   [Gravando filtro de endereços de endereço](writing-addresstable-filter-portion.md)
-   [Gravando o filtro PATTERNMATCH](writing-the-patternmatch-filter.md)
-   [Recortando um quadro](clipping-a-frame.md)
-   [Implementando o código de filtro de captura](implementing-the-capture-filter-code.md)

Um [*filtro de captura*](c.md) é uma série de adições ao blob NPP que seleciona quais quadros são passados de volta para o monitor. Se um monitor não alterar o BLOB NPP, o NPP entrará no modo promíscuo e enviará todo o tráfego de rede para o monitor. O NPP será mais eficiente se puder reduzir os dados entregues a um driver, de modo que um monitor deve criar um filtro de captura. Um monitor define seu filtro de captura gravando no BLOB NPP na chamada à função [doconfigure](imonitor-doconfigure.md) . Em seguida, o MCSVC chama o NPP com o BLOB NPP. Consulte [filtros de captura](capture-filters.md) para obter mais detalhes sobre o filtro de captura, [provedores de pacotes de rede](network-packet-providers.md) em NPPs e [Monitor de rede BLOBs](network-monitor-blobs.md) em funções de BLOB.

 

 



