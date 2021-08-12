---
description: Registrando e desregulando chaves
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrando e desregulando chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d586fc2bf399a30b8a962611a21a4e0994d88f4513453c071b110de1d4142b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612159"
---
# <a name="registering-and-deregistering-keys"></a>Registrando e desregulando chaves

## <a name="registering-keys"></a>Registrando chaves

Um nó pode registrar chaves com [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) a qualquer momento enquanto estiver nos estados **DRT \_ ACTIVE,** **DRT \_ ALONE** e **DRT \_ NO \_ NETWORK.** As chaves registradas **nos estados DRT \_ ALONE** e **DRT NO \_ \_ NETWORK** só poderão ser reconhecidas por outros DRTs depois que o nó local tiver feito a transição para **DRT \_ ACTIVE.**

Chaves idênticas não podem ser registradas na mesma instância DRT ao usar [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider). Se o registro de chaves idênticas for tentado, o registro da segunda chave falhará. O uso de chaves idênticas também deve ser evitado entre diferentes instâncias drt. Pesquisa na designação de chave exclusiva que esses compartilhamentos de chaves idênticas podem retornar qualquer uma das chaves, independentemente de quais dados estão associados à chave.

> [!Note]  
> Se um comportamento diferente for necessário para implementação, um provedor de segurança poderá ser criado no lugar de [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) para acomodar.

 

## <a name="deregistering-keys"></a>Desregisando chaves

Um nó pode desregister uma chave a qualquer momento depois que ela tiver sido registrada. No entanto, somente o aplicativo que registrou a chave pode desregisá-la. Um aplicativo pode desregister uma chave do nó local usando a [**função DrtUnregisterKey.**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) Após a conclusão, a função dispara um evento **DRT \_ EVENT \_ LEAFSET \_ KEY \_ CHANGE;** informando o aplicativo, bem como outros nós que participam da malha DRT.

Enquanto estiver no **estado DRT \_ FAULTED,** a chamada necessária de [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) resultará na desregulamentação de todas as chaves da infraestrutura drt.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisando uma tabela de roteamento distribuída](searching-a-distributed-routing-table.md)
</dt> <dt>

[Sobre tabelas de roteamento distribuído](about-distributed-routing-tables.md)
</dt> <dt>

[Referência de API de Tabela roteamento distribuído](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



