---
description: Ao criar um objeto seguro, você pode atribuir um descritor de segurança ao novo objeto.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Descritores de segurança para novos objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38edc927f1f017e3f102194b0a4aac5d0442ec730e8480a00c054add0935a62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907336"
---
# <a name="security-descriptors-for-new-objects"></a>Descritores de segurança para novos objetos

Ao criar um objeto seguro, você pode atribuir um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) ao novo objeto. As funções para criar objetos de segurança, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**RegCreateKeyEx,**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)têm um parâmetro que aponta para a estrutura [**ATRIBUTOS \_ DE**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) SEGURANÇA que podem conter um ponteiro para o descritor de segurança do novo objeto. Para um código de exemplo que cria um descritor de segurança e, em seguida, chama **RegCreateKeyEx** para atribuir o descritor de segurança a uma nova chave do Registro, consulte Criando um descritor de segurança para um novo objeto [em C++.](creating-a-security-descriptor-for-a-new-object-in-c--.md)

O componente do sistema ou servidor que gerencia o objeto pode armazenar o descritor de segurança especificado ou padrão para torná-lo um atributo persistente do objeto. Se o criador de um objeto não especificar um descritor de segurança, o sistema usará informações de segurança herdadas ou padrão para criar um descritor de segurança. Você pode usar funções para alterar as informações no descritor de segurança de um objeto.

Objetos de serviço de diretório, arquivos, diretórios, chaves do Registro e áreas de trabalho são objetos que podem ter um objeto pai. Quando você cria um desses objetos, o sistema verifica se há ACEs herdáveis no descritor de segurança do objeto pai. O sistema normalmente mescla todas as ACEs herdáveis nas ACLs do descritor de segurança do novo objeto. Você pode impedir que uma DACL ou SACL herde ACEs definindo os bits protegidos por DACL ES ou \_ \_ ES \_ SACL PROTECTED nos bits de controle do descritor de \_ segurança. Para obter mais informações, consulte [HERANÇA ACE.](ace-inheritance.md)

 

 
