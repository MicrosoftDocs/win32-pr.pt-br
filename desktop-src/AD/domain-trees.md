---
title: Árvores de domínio
description: Uma árvore de domínio é formada por vários domínios que compartilham um esquema e uma configuração comuns, formar um namespace contíguo.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- árvore de domínio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a1e2ed05284d2a08735b048fb41d97d6597634f711094d0a3763c2d7f8be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430504"
---
# <a name="domain-trees"></a>Árvores de domínio

Uma *árvore de* domínio é formada por vários domínios que compartilham um esquema e uma configuração comuns, formar um namespace contíguo. Os domínios em uma árvore também são vinculados por relações de confiança. O Active Directory é um conjunto de uma ou mais árvores.

As árvores podem ser exibidas de duas maneiras. Uma exibição são as relações de confiança entre domínios. A outra exibição é o namespace da árvore de domínio.

## <a name="viewing-trust-relationships"></a>Exibindo relações de confiança

Você pode desenhar um diagrama de uma árvore de domínio com base nos domínios individuais e na relação de confiança existente.

Windows 2000 estabelece relações de confiança entre domínios com base no protocolo de segurança Kerberos. A confiança kerberos é transitiva e hierárquica— se o domínio A confiar no domínio B e o domínio B confiar no domínio C, o domínio A confiará no domínio C.

![relação de confiança da árvore de domínio](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>Exibindo o namespace

Você também pode desenhar um diagrama de uma árvore de domínio com base no namespace . Você pode determinar o nome diferenciado de um objeto seguindo o caminho até a hierarquia do namespace da árvore de domínio. Essa exibição é útil para agrupar objetos em uma hierarquia lógica. A principal vantagem de um namespace contíguo é que uma pesquisa profunda na raiz do namespace pesquisa toda a hierarquia.

![árvore de domínio do namespace](images/namespace.png)

 

 




