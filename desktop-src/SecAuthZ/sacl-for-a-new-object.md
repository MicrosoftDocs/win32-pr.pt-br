---
description: SACL para um novo objeto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL para um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f9833fcfb45a612b6135579e44aca6f219661fd2aeb2998b899e5794fa7bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413836"
---
# <a name="sacl-for-a-new-object"></a>SACL para um novo objeto

O sistema usa o seguinte algoritmo para criar uma SACL para a maioria dos tipos de novos objetos de segurança:

1.  A SACL do objeto é a SACL do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) especificado pelo criador do objeto. O sistema mescla todas as ACEs herdáveis na SACL especificada, a menos que o bit ES SACL PROTECTED esteja definido nos bits de controle do descritor \_ \_ de segurança. ACEs de ATRIBUTO DE RECURSO DO SISTEMA e ACEs de ID DE POLÍTICA COM ESCOPO DO SISTEMA de um objeto pai serão mescladas a um novo objeto, mesmo se o bit ES \_ \_ \_ \_ \_ \_ \_ \_ SACL \_ PROTECTED estiver definido.
2.  Se o criador não especificar um descritor de segurança, o sistema criará a SACL do objeto de ACEs herdáveis.
3.  Se não houver NENHUM SACL especificado ou herdado, o objeto não terá SACL.

Para especificar uma SACL para um novo objeto, o criador do objeto deve ter o privilégio ES \_ SECURITY \_ [NAME](privileges.md) habilitado. Se a SACL especificada para um novo objeto contém apenas ACEs DE ATRIBUTO DE RECURSO DO SISTEMA, o privilégio \_ ES SECURITY NAME não é \_ \_ \_ \_ necessário. O criador não precisará desse privilégio se a SACL do objeto for criada com base em ACEs herdadas.

O sistema usa um algoritmo diferente para criar uma SACL para um novo objeto do Active Directory. Para obter mais informações, consulte [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
