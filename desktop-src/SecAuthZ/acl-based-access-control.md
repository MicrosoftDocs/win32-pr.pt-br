---
description: Assim como o sistema usa descritores de segurança para controlar o acesso a objetos protegíveis, um servidor pode usar descritores de segurança para controlar o acesso a seus objetos privados. para obter mais informações sobre o modelo de segurança Windows, consulte modelo de controle de acesso.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Controle de acesso baseado em ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52867b78114474e1b7827bddf8fd17cd2f3fd71cd88b62cff25397e8bab9b4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785161"
---
# <a name="acl-based-access-control"></a>Controle de acesso baseado em ACL

Assim como o sistema usa [descritores de segurança](security-descriptors.md) para controlar o acesso a objetos protegíveis, um servidor pode usar descritores de segurança para controlar o acesso a seus objetos privados. para obter mais informações sobre o modelo de segurança Windows, consulte [modelo de controle de acesso](access-control-model.md).

Um servidor protegido pode [criar um descritor de segurança](security-descriptors-for-private-objects.md) com uma DACL que especifica os tipos de acesso permitidos para vários dos [confiáveis](trustees.md). Em um caso simples, o servidor pode criar um único descritor de segurança para [controlar o acesso a todos os dados e funcionalidades do servidor](checking-access-to-private-objects.md). Para uma granularidade mais refinada de proteção, o servidor pode criar descritores de segurança para cada um de seus objetos privados ou para diferentes tipos de funcionalidade.

Por exemplo, quando um cliente solicita que o servidor crie um novo objeto em um banco de dados, o servidor pode criar um descritor de segurança para o novo objeto privado. O servidor poderia então armazenar o descritor de segurança com o objeto particular no banco de dados. Quando um cliente tenta acessar o objeto, o servidor recupera o descritor de segurança para verificar os direitos de acesso do cliente. É importante observar que não há nada em um descritor de segurança que o associe com o objeto ou a funcionalidade que ele está protegendo. Em vez disso, cabe ao servidor protegido manter a associação.

O acesso ao objeto particular também pode ser auditado. Consulte [auditoria de acesso a objetos privados](auditing-access-to-private-objects.md) para obter uma descrição disso.

 

 



