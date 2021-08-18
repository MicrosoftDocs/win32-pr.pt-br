---
title: Adicionando uma reserva
description: O banco de dados de roteamento contém a lista de reservas.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac683c48748fa0e644f2f7569590b3783c521f1d10a1a5852a638a29731daf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014944"
---
# <a name="adding-a-reservation"></a>Adicionando uma reserva

O banco de dados de roteamento contém a lista de reservas. A lista de reservas consiste nos usuários que têm permissão de acesso ao namespace, bem como o nível de acesso para cada usuário listado na reserva. Quando as reservas são adicionadas ou excluídas, o banco de dados de roteamento é pesquisado para determinar os privilégios de acesso.

Além de verificar a ID dos usuários, a API do Servidor HTTP também verifica se há conflitos em reservas existentes antes de instalar uma nova reserva.

**Para adicionar uma nova reserva**

1.  Se o número da porta em UrlPrefix tiver reservas ou registros para um esquema diferente do esquema em UrlPrefix, o registro falhará. HTTP e HTTPS não podem ser suportados na mesma porta.
2.  Localize o bucket apropriado para o registro (consulte a seção [Roteamento de](routing-incoming-requests.md) solicitações de entrada), com base no tipo de host. As etapas restantes são relativas a esse bucket.
3.  Selecione entradas de reserva com componentes de esquema, host e porta que corresponderem ao UrlPrefix que está sendo reservado. Desses, localize a entrada com o *relativeUri* correspondente mais longo que não é igual ao relativeUri na reserva (ou seja, *o nó pai*). Se a entrada existir, avalie os direitos de acesso com base na ACL atribuída a essa entrada.
4.  Se um nó pai não foi encontrado, essa é uma reserva com um relativeUri vazio ou *reserva raiz*. Conceda direitos de acesso somente se o chamador estiver registrado nas contas LocalSystem ou Administrador.
5.  Se os direitos de acesso são concedidos, verifique se há reservas duplicadas. Se existir uma entrada de reserva com o mesmo esquema, porta, host e relativeUri, um código ERROR \_ ALREADY \_ EXISTS será retornado.
    > [!Note]  
    > A atualização de uma entrada existente deve ser executada em duas etapas: excluir a entrada e adicionar uma nova.

     

Se as etapas acima são bem-sucedidas, uma nova entrada de reserva é inserida no banco de dados de reserva.

> [!Note]  
> A nova entrada é criada com a ACL especificada e não herda ACLs da *entrada* pai.

 

Os exemplos a seguir ilustram o processo de reserva.

-   Reserva 1: por Administrador para Usuário A e Usuário C é bem-sucedido e `https://+:80/vroot/subdir/` é inserido no bucket "+".
-   Reserva 2: `https://adatum.com:80/vroot/` por Administrador para Usuário B é bem-sucedido e é inserido no bucket "Host explícito".
-   Reserva 3: `https://adatum.com:80/vroot/subdir/otherdir/` por Usuário B para Usuário C é bem-sucedido devido à reserva 2.
-   Reserva 4: `https://+:80/vroot/subdir/otherdir/` por Usuário A para Usuário E é bem-sucedido devido à reserva 1.
-   Reserva 5: `https://adatum.com:80/vroot/subdir/otherdir/` falha por Usuário A para Usuário E. Acesso negado devido à reserva 2.
-   Reserva 6: `https://+:80/vroot/subdir/` falha por Administrador para Usuário A. A reserva está em conflito com a reserva 1.
-   Reserva 7: `https://adatum.com:80/newroot/` falha por Usuário A para Usuário A. Acesso negado devido à reserva raiz implícita de `https://adatum.com:80/` para LocalSystem ou Administrador.

As reservas podem afetar o conjunto de URLs em solicitações entregues a um processo que registrou anteriormente um UrlPrefix. Por exemplo, considere o cenário a seguir.

-   Registro: `https://adatum.com:80/vroot/` pelo aplicativo 1 para o Usuário A.
-   Uma solicitação `https://adatum.com:80/vroot/subdir/file.htm` para é entregue ao aplicativo 1.
-   Reserva: `https://+:80/vroot/subdir/` para o Usuário B.
-   Uma solicitação `https://adatum.com:80/vroot/subdir/file.htm` para agora é rejeitada.
-   Registro: `https://adatum.com:80/vroot/subdir/` pelo aplicativo 2 para o Usuário B.
-   Uma solicitação `https://adatum.com:80/vroot/subdir/file.htm` para é entregue ao aplicativo 2.

 

 




