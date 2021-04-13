---
title: Adicionando uma reserva
description: O banco de dados de roteamento contém a lista de reserva.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104499182"
---
# <a name="adding-a-reservation"></a>Adicionando uma reserva

O banco de dados de roteamento contém a lista de reserva. A lista de reserva consiste nos usuários que têm permissão de acesso ao namespace, bem como o nível de acesso para cada usuário listado na reserva. Quando as reservas são adicionadas ou excluídas, o banco de dados de roteamento é pesquisado para determinar os privilégios de acesso.

Além de verificar a ID dos usuários, a API do servidor HTTP também verifica se há conflitos em reservas existentes antes de instalar uma nova reserva.

**Para adicionar uma nova reserva**

1.  Se o número da porta no UrlPrefix tiver reservas ou registros para um esquema diferente do esquema no UrlPrefix, o registro falhará. Não há suporte para HTTP e HTTPS na mesma porta.
2.  Localize o Bucket apropriado para o registro (consulte a seção [solicitações de entrada de roteamento](routing-incoming-requests.md) ), com base no tipo de host. As etapas restantes são relativas a esse Bucket.
3.  Selecione entradas de reserva com componentes de esquema, host e porta que correspondam ao UrlPrefix que está sendo reservado. A partir deles, localize a entrada com o *relativeUri* correspondente mais longo que não seja igual ao relativeUri na Reserva (ou seja, o *nó pai*). Se a entrada existir, avalie os direitos de acesso com base na ACL atribuída a essa entrada.
4.  Se um nó pai não foi encontrado, essa é uma reserva com uma relativeUri vazia ou *reserva de raiz*. Conceda direitos de acesso somente se o chamador estiver registrado nas contas LocalSystem ou administrador.
5.  Se direitos de acesso forem concedidos, verifique se há reservas duplicadas. Se existir uma entrada de reserva com o mesmo esquema, porta, host e relativeUri, um \_ código de erro já \_ existe será retornado.
    > [!Note]  
    > A atualização de uma entrada existente deve ser executada em duas etapas: excluir a entrada e adicionar uma nova.

     

Se as etapas acima forem realizadas com sucesso, uma nova entrada de reserva será inserida no banco de dados de reserva.

> [!Note]  
> A nova entrada é criada com a ACL especificada e não herda ACLs da entrada *pai* .

 

Os exemplos a seguir ilustram o processo de reserva.

-   Reserva 1: `https://+:80/vroot/subdir/` pelo administrador para o usuário A e o usuário C são bem-sucedidos e inseridos no Bucket "+".
-   Reserva 2: `https://adatum.com:80/vroot/` pelo administrador para o usuário B é bem sucedido e é inserido no Bucket "host explícito".
-   Reserva 3: `https://adatum.com:80/vroot/subdir/otherdir/` pelo usuário B para o usuário C teve sucesso devido à reserva 2.
-   Reserva 4: `https://+:80/vroot/subdir/otherdir/` pelo usuário A para o usuário E é realizada com sucesso devido à reserva 1.
-   Reserva 5: `https://adatum.com:80/vroot/subdir/otherdir/` pelo usuário A para o usuário E falha. Acesso negado devido à reserva 2.
-   Reserva 6: `https://+:80/vroot/subdir/` pelo administrador para o usuário A falha. A reserva está em conflito com a reserva 1.
-   Reserva 7: `https://adatum.com:80/newroot/` pelo usuário a para o usuário a falha. Acesso negado devido à reserva de raiz implícita de `https://adatum.com:80/` para LocalSystem ou administrador.

As reservas podem afetar o conjunto de URLs em solicitações entregues a um processo que registrou anteriormente um UrlPrefix. Por exemplo, considere o cenário a seguir.

-   Registro: `https://adatum.com:80/vroot/` por aplicativo 1 para o usuário A.
-   Uma solicitação para `https://adatum.com:80/vroot/subdir/file.htm` é entregue ao aplicativo 1.
-   Reserva: `https://+:80/vroot/subdir/` para o usuário B.
-   Uma solicitação para `https://adatum.com:80/vroot/subdir/file.htm` agora é rejeitada.
-   Registro: `https://adatum.com:80/vroot/subdir/` por aplicativo 2 para o usuário B.
-   Uma solicitação para `https://adatum.com:80/vroot/subdir/file.htm` é entregue ao aplicativo 2.

 

 




