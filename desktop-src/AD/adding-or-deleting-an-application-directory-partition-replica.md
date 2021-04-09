---
title: Adicionando ou excluindo uma réplica de partição de diretório de aplicativo
description: A primeira réplica de uma partição de diretório de aplicativo é criada no controlador de domínio que foi associado a ela no momento da criação.
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- Adicionando ou excluindo um AD de réplica de partição de diretório de aplicativo
- Partições de diretório de aplicativos AD, adicionando ou excluindo uma réplica de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c84b19e64f6abfc5e63d6e0e3d1b3a192da3e38
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084455"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a>Adicionando ou excluindo uma réplica de partição de diretório de aplicativo

A primeira réplica de uma partição de diretório de aplicativo é criada no controlador de domínio que foi associado a ela no momento da criação. Réplicas adicionais podem ser criadas em qualquer controlador de domínio na floresta, não necessariamente no mesmo domínio que o controlador de domínio inicial. Uma réplica de partição de diretório de aplicativo só pode existir em um controlador de domínio que esteja executando o Windows Server 2003 ou posterior. Para obter mais informações, consulte este artigo do TechNet sobre o [Gerenciamento de partição](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10)).

**Para adicionar uma réplica para uma partição de diretório de aplicativo, execute as seguintes etapas**

1.  Pesquise o contêiner partições para obter um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenha um valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) igual ao nome distinto da partição de diretório do aplicativo.
2.  Associar ao objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) com delegação habilitada. Isso é necessário porque o objeto **crossRef** só pode ser modificado no detentor da função FSMO Domain-Naming. Com a delegação habilitada, o controlador de domínio pode entrar em contato com o detentor da função FSMO Domain-Naming usando as mesmas credenciais.
3.  Adicione o nome distinto do objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para o controlador de domínio que hospedará a nova réplica para o atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

Quando o novo valor de atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) é replicado para o novo controlador de domínio que hospedará uma réplica da partição de diretório de aplicativo, o KCC será disparado para replicar a partição de diretório de aplicativo para o controlador de domínio de destino.

Para remover uma réplica de uma partição de diretório de aplicativo, execute as mesmas etapas acima para localizar o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório de aplicativo e remover o valor que corresponde ao controlador de domínio do atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) do objeto **crossRef** .

Quando o novo valor de atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) é replicado para o controlador de domínio que não hospedará mais uma réplica da partição de diretório de aplicativo, o KCC será disparado para remover a réplica da partição de diretório de aplicativo no controlador de domínio de destino.

Se um controlador de domínio que está hospedando uma réplica de partição de diretório de aplicativos for removido ou rebaixado, o servidor de Active Directory removerá automaticamente o valor correspondente ao controlador de domínio do atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de todos os objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

 

 