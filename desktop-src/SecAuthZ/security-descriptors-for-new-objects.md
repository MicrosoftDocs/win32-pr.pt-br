---
description: Ao criar um objeto protegível, você pode atribuir um descritor de segurança ao novo objeto.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Descritores de segurança para novos objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3f9af674c83e4fc42448635bc54dfc0bb51b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756164"
---
# <a name="security-descriptors-for-new-objects"></a>Descritores de segurança para novos objetos

Ao criar um objeto protegível, você pode atribuir um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) ao novo objeto. As funções para criar objetos protegíveis, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa), têm um parâmetro que aponta para a estrutura [**de \_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) que pode conter um ponteiro para o descritor de segurança do novo objeto. Para obter um código de exemplo que cria um descritor de segurança e, em seguida, chama **RegCreateKeyEx** para atribuir o descritor de segurança a uma nova chave do registro, consulte [criando um descritor de segurança para um novo objeto em C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).

O componente do sistema ou servidor que gerencia o objeto pode armazenar o descritor de segurança padrão ou especificado para torná-lo um atributo persistente do objeto. Se o criador de um objeto não especificar um descritor de segurança, o sistema usará as informações de segurança herdadas ou padrão para criar um descritor de segurança. Você pode usar funções para alterar as informações no descritor de segurança de um objeto.

Os objetos do serviço de diretório, os arquivos, os diretórios, as chaves do registro e as áreas de trabalho são objetos protegíveis que podem ter um objeto pai. Quando você cria um desses objetos, o sistema verifica ACEs herdáveis no descritor de segurança do objeto pai. O sistema normalmente mescla quaisquer ACEs herdáveis nas ACLs do descritor de segurança do novo objeto. Você pode impedir que uma DACL ou SACL herde ACEs Configurando os \_ bits se a DACL protegida \_ ou se estiverem protegidos por \_ SACL \_ nos bits de controle do descritor de segurança. Para obter mais informações, consulte [Ace Inheritance](ace-inheritance.md).

 

 
