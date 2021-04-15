---
title: A porta 3 foi preterida para drivers NDIS 6,30
description: A porta 3 foi preterida para drivers NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104454409"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a>A porta 3 foi preterida para drivers NDIS 6,30

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

O Windows 8 remove o suporte de plataforma para drivers WLAN da miniporta NDIS para criar ou iniciar a porta de extensibilidade do IHV (também conhecida como 3ª porta). Esse recurso foi introduzido no Windows 7 como uma medida paliativa enquanto a WFA (Aliança de Wi-Fi) desenvolveu a especificação Wi-Fi Direct. A especificação agora está concluída, os produtos que usam Wi-Fi Direct estão sendo certificados e o Windows 8 introduz uma pilha nativa Wi-Fi Direct.

## <a name="manifestation"></a>Manifestação

Nada, pois a terceira porta é uma funcionalidade de plataforma que os drivers de miniporta WLAN iniciam se precisarem dessa funcionalidade.

## <a name="solution"></a>Solução

Estamos mantendo o recurso de porta de extensibilidade disponível para drivers existentes que não relatam o NDIS 6,30 para manter a compatibilidade do dispositivo. No entanto, novos drivers WLAN que relatam a NDIS 6,30 não poderão iniciar essa porta; em vez disso, os desenvolvedores desses drivers devem usar o Wi-Fi Direct.

 

 




