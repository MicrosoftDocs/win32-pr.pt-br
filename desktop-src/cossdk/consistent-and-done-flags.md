---
description: Sinalizadores consistentes e concluídos
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Sinalizadores consistentes e concluídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501130"
---
# <a name="consistent-and-done-flags"></a>Sinalizadores consistentes e concluídos

O COM+ sempre cria um objeto de contexto antes de ativar um objeto transacional. O objeto de contexto contém informações relacionadas a objeto, como seu criador e seu identificador de transação. Cada objeto de contexto também contém um *sinalizador consistente* e um *sinalizador Done*. Juntos, esses sinalizadores determinam o status do objeto transacional.

O sinalizador consistente indica que o objeto transacional é consistente ou inconsistente. Os detalhes específicos do que tornam o estado do objeto consistente é o programador. Quando uma chamada de método define esse sinalizador como true, o objeto é consistente. False indica que o objeto está inconsistente. COM+ define o sinalizador como true quando ele cria uma instância de objeto. Um objeto consistente está pronto para prosseguir com a transação. Enquanto um objeto permanece ativo, as chamadas de método subsequentes podem alternar repetidamente o sinalizador consistente de verdadeiro para falso e vice-versa.

O sinalizador Done determina a duração de uma transação. Quando uma chamada de método retorna, o COM+ inspeciona o sinalizador done. Se o método definir esse sinalizador como true, o COM+ desativará o objeto e notará o sinalizador consistente. Quando o sinalizador Done é false, COM+ não desativa o objeto nem anota o sinalizador consistente. COM+ define o sinalizador Done como false quando ele cria uma instância de objeto.

O sinalizador consistente converte um voto para confirmar ou anular a transação na qual ele é executado, e o sinalizador concluído finaliza o voto. O COM+ inspeciona o sinalizador consistente quando o sinalizador Done é definido como true em um retorno de chamada de método ou quando o objeto é desativado. Embora o sinalizador consistente de um objeto possa ser alterado repetidamente dentro de cada chamada de método, somente as últimas contagens de alteração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando transações automáticas no COM+](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[Definindo os sinalizadores consistentes e concluídos](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



