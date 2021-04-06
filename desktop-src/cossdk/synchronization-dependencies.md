---
description: Os valores de sincronização podem ser determinados ou restritos automaticamente pela configuração de outras propriedades, como requisitos transacionais e ativação JIT (just-in-time).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dependências de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826314"
---
# <a name="synchronization-dependencies"></a>Dependências de sincronização

Os valores de sincronização podem ser determinados ou restritos automaticamente pela configuração de outras propriedades, como requisitos transacionais e ativação JIT (just-in-time). Por exemplo, COM+ impõe a sincronização para os componentes transacionais e ativados por JIT.

Essas dependências existem porque os componentes que são ativados por JIT ou que participam de transações devem ter isolamento adequado e comportamento de simultaneidade. Portanto, o COM+ exige que o acesso a esses componentes seja serializado por meio da imposição da sincronização. (Para obter detalhes sobre essas dependências, consulte [ativação Just-in-time do com+](com--just-in-time-activation.md).)

As tabelas a seguir mostram as características dos valores de atributo de sincronização COM+.

### <a name="transactional-requirement"></a>Requisito transacional



| Quando as transações são definidas como | A sincronização pode ser definida como                    |
|------------------------------|--------------------------------------------------|
| Desabilitado<br/>          | Qualquer coisa, dependendo da ativação JIT<br/> |
| Sem suporte<br/>     | Qualquer coisa, dependendo da ativação JIT<br/> |
| Com suporte<br/>         | Obrigatório<br/>                              |
| Obrigatório<br/>          | Obrigatório<br/>                              |
| Requer novo<br/>      | Necessário ou requer novo<br/>              |



 

### <a name="jit-activation"></a>Ativação JIT



| Quando a ativação JIT é definida como | A sincronização pode ser definida como       |
|-------------------------------|-------------------------------------|
| habilitado<br/>            | Necessário ou requer novo<br/> |
| Desabilitado<br/>           | Dado<br/>                 |



 

Para obter mais detalhes sobre como a transação, ativação JIT e atributos de sincronização se comportam, consulte [Configurando transações](configuring-transactions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o atributo de sincronização](setting-the-synchronization-attribute.md)
</dt> <dt>

[Valores de atributo de sincronização](synchronization-attribute-values.md)
</dt> </dl>

 

 




