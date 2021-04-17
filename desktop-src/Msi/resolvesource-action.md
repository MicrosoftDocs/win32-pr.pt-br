---
description: A ação resolver determina o local da origem e define a propriedade SourceDir se a fonte ainda não tiver sido resolvida.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Ação resolver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787494"
---
# <a name="resolvesource-action"></a>Ação resolver

A ação resolver determina o local da origem e define a propriedade [**SourceDir**](sourcedir.md) se a fonte ainda não tiver sido resolvida.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação de resolução deve vir após a [ação CostInitialize](costinitialize-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

## <a name="remarks"></a>Comentários

A ação de resolução deve ser chamada antes de usar a propriedade [**SourceDir**](sourcedir.md) em qualquer expressão. Ele também deve ser chamado antes de tentar recuperar o valor da propriedade **SourceDir** usando [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). A ação de resolução não deve ser executada quando a origem não estiver disponível, pois pode ser ao desinstalar o aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 



