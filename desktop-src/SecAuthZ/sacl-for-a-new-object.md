---
description: SACL para um novo objeto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL para um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747504"
---
# <a name="sacl-for-a-new-object"></a>SACL para um novo objeto

O sistema usa o seguinte algoritmo para criar uma SACL para a maioria dos tipos de novos objetos protegíveis:

1.  A SACL do objeto é a SACL do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) especificado pelo criador do objeto. O sistema mescla quaisquer ACEs herdáveis na SACL especificada, a menos que o \_ \_ bit se protegido por SACL seja definido nos bits de controle do descritor de segurança. \_As ACEs \_ \_ de atributo de recurso do sistema e \_ \_ \_ \_ a ID da política no escopo do sistema ACEs de um objeto pai serão mescladas a um novo objeto, mesmo se o \_ bit protegido da SACL \_ estiver definido.
2.  Se o criador não especificar um descritor de segurança, o sistema criará a SACL do objeto de ACEs herdáveis.
3.  Se não houver nenhuma SACL especificada ou herdada, o objeto não terá nenhuma SACL.

Para especificar uma SACL para um novo objeto, o criador do objeto deve ter o \_ \_ [privilégio](privileges.md) nome de segurança se habilitado. Se a SACL especificada para um novo objeto contiver somente \_ ACEs de atributo de recurso \_ \_ do sistema, o \_ privilégio de nome de segurança se \_ não será necessário. O criador não precisará desse privilégio se a SACL do objeto for criada a partir de ACEs herdadas.

O sistema usa um algoritmo diferente para criar uma SACL para um novo objeto Active Directory. Para obter mais informações, consulte [como descritores de segurança são definidos em novos objetos de diretório](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
