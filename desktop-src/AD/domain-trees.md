---
title: Árvores de domínio
description: Uma árvore de domínio é composta por vários domínios que compartilham um esquema e uma configuração comuns, formando um namespace contíguo.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Active Directory de árvore de domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159332"
---
# <a name="domain-trees"></a>Árvores de domínio

Uma *árvore de domínio* é composta por vários domínios que compartilham um esquema e uma configuração comuns, formando um namespace contíguo. Os domínios em uma árvore também são vinculados por relações de confiança. Active Directory é um conjunto de uma ou mais árvores.

As árvores podem ser exibidas de duas maneiras. Uma exibição é a relação de confiança entre domínios. A outra exibição é o namespace da árvore de domínio.

## <a name="viewing-trust-relationships"></a>Exibindo relações de confiança

Você pode desenhar um diagrama de uma árvore de domínio com base nos domínios individuais e na relação de confiança existente.

O Windows 2000 estabelece relações de confiança entre domínios com base no protocolo de segurança Kerberos. A confiança Kerberos é transitiva e hierárquica – se o domínio A confiar no domínio B e o domínio B confiar no domínio C, o domínio A confiará no domínio C.

![relação de confiança da árvore de domínio](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>Exibindo o namespace

Você também pode desenhar um diagrama de uma árvore de domínio com base no namespace. Você pode determinar o nome distinto de um objeto seguindo o caminho para cima na hierarquia do namespace da árvore de domínio. Essa exibição é útil para agrupar objetos em uma hierarquia lógica. A principal vantagem de um namespace contíguo é que uma pesquisa profunda da raiz do namespace pesquisa toda a hierarquia.

![árvore de domínio de namespace](images/namespace.png)

 

 




