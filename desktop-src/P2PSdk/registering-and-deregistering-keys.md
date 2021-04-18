---
description: Registrando e cancelando o registro de chaves
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrando e cancelando o registro de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753111"
---
# <a name="registering-and-deregistering-keys"></a>Registrando e cancelando o registro de chaves

## <a name="registering-keys"></a>Registrando chaves

Um nó pode registrar chaves com [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) a qualquer momento enquanto nos Estados de rede **DRT \_ ativa**, **DRT \_ sozinha** e **DRT \_ não \_** . Chaves registradas em **DRT \_ sozinha** e **DRT nenhum estado de \_ \_ rede** só pode ser reconhecido por outros DRTs depois que o nó local tiver feito a transição para a **DRT \_ ativa**.

Chaves idênticas não podem ser registradas na mesma instância de DRT ao usar [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider). Se o registro de chaves idênticas for tentado, o registro da segunda chave falhará. O uso de chaves idênticas também deve ser evitado entre diferentes instâncias de DRT. Pesquisa na designação de chave exclusiva essas chaves idênticas compartilhadas podem retornar qualquer uma das chaves, independentemente de quais dados estão associados à chave.

> [!Note]  
> Se um comportamento diferente for necessário para a implementação, um provedor de segurança poderá ser criado no lugar do [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) para acomodar.

 

## <a name="deregistering-keys"></a>Cancelando o registro de chaves

Um nó pode cancelar o registro de uma chave a qualquer momento depois de ser registrado. No entanto, somente o aplicativo que registrou a chave pode cancelar seu registro. Um aplicativo pode cancelar o registro de uma chave do nó local usando a função [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) . Após a conclusão, a função dispara um evento de alteração de chave de tipo folha de um **\_ evento \_ \_ \_ DRT** ; informando o aplicativo, bem como outros nós que participam da malha DRT.

Enquanto estiver no estado **DRT \_ com falha** , a chamada necessária de [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) resultará na desregistro de todas as chaves na infraestrutura DRT.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisando uma tabela de roteamento distribuída](searching-a-distributed-routing-table.md)
</dt> <dt>

[Sobre tabelas de roteamento distribuído](about-distributed-routing-tables.md)
</dt> <dt>

[Referência de API de Tabela de roteamento distribuído](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



