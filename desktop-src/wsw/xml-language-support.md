---
title: Suporte à linguagem XML
description: Esta seção descreve o nível de suporte à linguagem XML no WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Serviços Web de suporte de linguagem XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105750875"
---
# <a name="xml-language-support"></a>Suporte à linguagem XML

Esta seção descreve o nível de suporte à linguagem XML no WWS.


Consulte as funções DownlevelLCIDToLocaleName em versões do Windows anteriores ao Windows Vista e LCIDToLocalName, caso contrário, para converter entre um LCID e um valor XML: lang.

Ao ler, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) pode ser usado para descobrir o valor de um atributo "XML: lang" no escopo.

Durante a gravação, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) pode ser usado para gravar um atributo "XML: lang".

 

 




