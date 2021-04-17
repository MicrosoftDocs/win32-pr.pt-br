---
description: A capacidade do Windows Installer de definir permissões de acesso em serviços, arquivos, pastas criadas e entradas de registro pode ajudar a tornar os aplicativos de instalação mais seguros.
ms.assetid: a25fcecf-f15f-4772-8f41-d03864484cc9
title: Protegendo recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415fe7b2df343a54aa0819031f4fd22b05857618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749574"
---
# <a name="securing-resources"></a>Protegendo recursos

A capacidade do Windows Installer de definir permissões de acesso em serviços, arquivos, pastas criadas e entradas de registro pode ajudar a tornar os aplicativos de instalação mais seguros. O uso das tabelas [MsiLockPermissionsEx](msilockpermissionsex-table.md) ou [LockPermissions](lockpermissions-table.md) para proteger recursos é uma das diretrizes recomendadas [para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md). A tabela MsiLockPermissionsEx pode permitir que um autor de pacote proteja um recurso sem precisar escrever uma [ação personalizada](custom-actions.md).

A partir de pacotes desenvolvidos para o Windows Installer 5,0, a tabela [MsiLockPermissionsEx](msilockpermissionsex-table.md) deve substituir o uso da tabela [LockPermissions](lockpermissions-table.md) . A funcionalidade estendida fornecida pela tabela MsiLockPermissionsEx permite que um pacote proteja os [Serviços](../services/services.md), arquivos, pastas e chaves do registro do Windows. Um pacote não deve conter as tabelas MsiLockPermissionsEx e LockPermissions.

Windows Installer 4,5 e anterior ignora a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md). A partir do Windows Installer 5,0, a instalação falhará com uma mensagem de erro 1941 se o pacote contiver uma [Tabela LockPermissions](lockpermissions-table.md) e uma tabela MsiLockPermissionsEx. Os pacotes de instalação existentes que contêm apenas a Tabela LockPermissions ainda podem ser instalados usando Windows Installer 5,0.

Windows Installer 5,0 processa as informações na tabela [MsiLockPermissionsEx](msilockpermissionsex-table.md) quando executa as ações padrão [InstallFiles](installfiles-action.md), [installservices](installservices-action.md), [WriteRegistryValues](writeregistryvalues-action.md) e [createfolders](createfolders-action.md) . Um objeto protegível deve ser instalado ou reinstalado para ser protegido e não é possível acrescentar uma [lista de controle de acesso](../secauthz/access-control-lists.md) (ACL) a um objeto existente sem reinstalar esse objeto.

Para especificar o serviço, o arquivo, o diretório ou a chave do registro a ser protegida, insira as informações de identificação nos campos lockobject e Table da tabela [MsiLockPermissionsEx](msilockpermissionsex-table.md) . Um objeto é identificado pela chave primária na [tabela](serviceinstall-table.md), na tabela de [arquivos](file-table.md), na tabela [do registro](registry-table.md)ou na tabela [CreateFolder](createfolder-table.md).

Para solicitar que as permissões especificadas se apliquem a um objeto, insira uma cadeia de caracteres de descritor de segurança válida no campo *SDDLText* da tabela [MsiLockPermissionsEx](msilockpermissionsex-table.md) usando uma SDDL ( [linguagem de definição de descritor de segurança](../secauthz/security-descriptor-definition-language.md) ) válida. A tabela **MsiLockPermissionsEx** pode especificar um descritor de segurança que nega permissões, especifica a herança de permissões de um recurso pai ou especifica as permissões de uma nova conta. Para obter uma lista de todas as permissões que podem ser concedidas, negadas ou herdadas, consulte [seqüências de caracteres Ace](../secauthz/ace-strings.md). Windows Installer 5,0 estende o conjunto de SIDs (identificadores de segurança) disponíveis. Para obter uma lista dos SIDs válidos, consulte [cadeias de caracteres de Sid](../secauthz/sid-strings.md).

> [!NOTE]
> Se você quiser configurar o descritor de segurança de um recurso pai para especificar que suas permissões sejam herdadas por objetos filho, o instalador deverá aplicar permissões ao recurso pai antes de criar os objetos filho. Se o instalador criar os objetos filho antes de aplicar as permissões herdáveis ao recurso pai, as permissões do recurso pai não serão propagadas para os objetos filho.

A partir do Windows Installer 5,0, o tipo de dados [FormattedSDDLText](formattedsddltext.md) estende o tipo de dados [formatado](formatted.md) . O Windows Installer valida que a cadeia de caracteres FormattedSDDLText inserida na coluna SDDLText da tabela [MsiLockPermissionsEx](msilockpermissionsex-table.md) está de acordo com o [formato de cadeia de caracteres do descritor de segurança](../secauthz/security-descriptor-string-format.md).

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. A tabela [MsiLockPermissionsEx](msilockpermissionsex-table.md) e o tipo de dados [FormattedSDDLText](formattedsddltext.md) estão disponíveis a partir do Windows Installer 5,0.

 

 
