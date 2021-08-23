---
title: Tipo de inicialização do BITS
description: O tipo de inicialização para BITS é um início automático atrasado. antes do Windows Vista, o tipo de inicialização para BITS é Manual. Quando um trabalho do BITS é criado, o tipo de inicialização muda para automático. O tipo de inicialização retorna para manual quando todos os trabalhos são concluídos ou cancelados.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: defafff5b3dd0a9b03e18b61b84fa6c32022035ce58913599151ee526fd52d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579426"
---
# <a name="bits-startup-type"></a>Tipo de inicialização do BITS

O **tipo de inicialização** para bits é o início automático atrasado (se houver trabalhos bits ativos) ou início da demanda (se não houver trabalhos ativos). versões de Windows antes da atualização de novembro usaram apenas o tipo de inicialização de início automático atrasado; versões anteriores ao vista usaram o tipo de inicialização manual.

Você não deve definir o **tipo de inicialização** como desabilitado. Desabilitar BITS pode interromper aplicativos que dependem de BITS para transferir arquivos.

 

 




