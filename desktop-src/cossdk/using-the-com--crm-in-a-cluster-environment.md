---
description: Usando o CRM do COM+ em um ambiente de cluster
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Usando o CRM do COM+ em um ambiente de cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a2d0800f98c9453e7d4454cdd59185dffb837649e391ebc415c965bee6ff80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499526"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>Usando o CRM do COM+ em um ambiente de cluster

Ao desenvolver o CRMs do COM+ para trabalhar em ambientes de cluster, o principal fator a ser considerado é se um CRM específico se preocupa com o nó do cluster em que ele está operando. Por exemplo, se o recurso gerenciado pelo CRM for o sistema de arquivos da máquina ou o registro, todas as alterações serão específicas para o nó em que o aplicativo do servidor do CRM está sendo executado no momento. Nesse caso, o failover do aplicativo do servidor do CRM para outro nó não seria desejável. Em um caso diferente, em que o CRM está gerenciando algum recurso comum ao cluster, o failover do aplicativo do servidor do CRM para outro nó é útil.

O local do diretório padrão para os arquivos de log do CRM é o mesmo diretório do arquivo de log do DTC. Em clusters, o arquivo de log do DTC é colocado em um disco compartilhado que faz failover entre os nós do cluster. Isso significa que o comportamento padrão para aplicativos do servidor CRM é fazer failover entre os nós do cluster. Portanto, se um CRM específico exigir o comportamento alternativo de não fazer failover entre os nós, o local do arquivo de log do CRM para esse aplicativo de servidor CRM específico deverá ser alterado.

Além disso, se o failover for necessário para o aplicativo CRM, ele deverá ser configurado como um aplicativo genérico em um grupo de clusters. Sua dependência deve ser DTC.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



