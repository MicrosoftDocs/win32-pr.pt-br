---
title: O que a instalação deve fazer
description: Os novos atributos referenciados na etapa 3 devem ser referenciados por seu OID porque o nome do novo atributo não está presente no cache de esquema neste ponto.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- O que a instalação deve fazer AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915927"
---
# <a name="what-the-installation-must-do"></a>O que a instalação deve fazer

Os aplicativos que estendem o esquema devem aplicar atualizações conforme descrito no procedimento a seguir.

**Para aplicar atualizações ao estender o esquema**

1.  Adicione os novos atributos.
2.  Adicione as novas classes.
3.  Adicione os novos atributos às classes.
4.  Disparar uma recarga de cache.

Os novos atributos referenciados na etapa 3 devem ser referenciados por seu OID porque o nome do novo atributo não está presente no cache de esquema neste ponto.

A etapa 4 é desnecessária se as extensões não forem usadas imediatamente; as extensões serão exibidas no cache de esquema em aproximadamente 5 minutos, dependendo da carga do sistema. Para obter mais informações sobre o cache de esquema e como disparar uma recarga de cache, consulte [atualizando o cache de esquema](updating-the-schema-cache.md).

 

 




