---
description: Os valores de sincronização podem ser determinados automaticamente ou restritos pela configuração de outras propriedades, como requisitos transacionais e ativação JIT (Just-In-Time).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dependências de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2976426d652ca50c4e7399f39e98ba13ef337d15ef8c15a2271d4a562d1790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499726"
---
# <a name="synchronization-dependencies"></a>Dependências de sincronização

Os valores de sincronização podem ser determinados automaticamente ou restritos pela configuração de outras propriedades, como requisitos transacionais e ativação JIT (Just-In-Time). Por exemplo, o COM+ impõe a sincronização para componentes transacionais e ativados por JIT.

Essas dependências existem porque os componentes ativados por JIT ou que participam de transações devem ter um comportamento adequado de isolamento e de competência. Portanto, o COM+ requer que o acesso a esses componentes seja serializado impondo a sincronização. (Para obter detalhes sobre essas dependências, consulte [COM+ Ativação Just-In-Time](com--just-in-time-activation.md).)

As tabelas a seguir mostram as características dos valores de atributo de sincronização COM+.

### <a name="transactional-requirement"></a>Requisito transacional



| Quando as transações são definidas como | A sincronização pode ser definida como                    |
|------------------------------|--------------------------------------------------|
| Desabilitado<br/>          | Qualquer coisa, dependendo da ativação JIT<br/> |
| Sem suporte<br/>     | Qualquer coisa, dependendo da ativação JIT<br/> |
| Com suporte<br/>         | Obrigatório<br/>                              |
| Obrigatório<br/>          | Obrigatório<br/>                              |
| Requer novo<br/>      | Obrigatório ou requer novo<br/>              |



 

### <a name="jit-activation"></a>Ativação JIT



| Quando a ativação JIT é definida como | A sincronização pode ser definida como       |
|-------------------------------|-------------------------------------|
| habilitado<br/>            | Obrigatório ou requer novo<br/> |
| Desabilitado<br/>           | Nada<br/>                 |



 

Para obter mais detalhes sobre como os atributos de transação, Ativação JIT e Sincronização se comportam juntos, consulte [Configurando transações](configuring-transactions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo o atributo de sincronização](setting-the-synchronization-attribute.md)
</dt> <dt>

[Valores de atributo de sincronização](synchronization-attribute-values.md)
</dt> </dl>

 

 




