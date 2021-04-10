---
title: ADSI e controle de conta de usuário
description: O Windows e o Windows Server têm controle de conta de usuário, que tem ramificações para aplicativos que usam ADSI (Active Directory Service Interfaces).
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008360"
---
# <a name="adsi-and-user-account-control"></a>ADSI e controle de conta de usuário

O Windows e o Windows Server têm [controle de conta de usuário](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), que tem ramificações para aplicativos que usam ADSI ( [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) ). Especificamente, essas interfaces foram projetadas para serem executadas por uma conta de usuário com privilégios de administrador no computador local.

**Problema**

Toda vez que um aplicativo se conecta ao diretório e tenta criar um objeto ADSI, o [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) é verificado quanto a alterações. Se ele foi alterado desde a última conexão, o esquema é baixado e armazenado em um cache no computador local. Em versões do Windows anteriores ao Windows Vista, o local padrão desse cache era

`%systemroot%\SchCache\`

No entanto, os aplicativos executados por contas padrão (ou seja, não administrador) não terão acesso a esse diretório e, consequentemente, os aplicativos que usam interfaces ADSI executadas nesse modo baixarão o esquema em cada conexão, o que afetará a taxa de transferência e o desempenho.

**Soluções**

*Usuário único* – para resolver esse problema, há novas chaves de controle do registro de provedor ADSI que determinam os locais de registro e os locais de arquivo para objetos de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) em cache. Se a chave do registro

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

é definido como 0 (zero), cada usuário terá um local de armazenamento diferente para ADSI; as chaves do registro serão armazenadas em

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

e os arquivos de cache serão armazenados em

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

Essas configurações são as configurações padrão em computadores que executam o Windows Server 2008 ou o Windows Vista.

*Multiusuário* – se você estiver executando aplicativos ADSI em um computador com muitas contas de usuário (por exemplo, um servidor Web), é preferível não ter muitas cópias do cache de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) usando grandes quantidades de espaço em disco. Configurando a chave do registro

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

para 1 (um), o ADSI será revertido para o comportamento anterior; todos os objetos de [esquema de Active Directory](/windows/desktop/ADSchema/active-directory-schema) serão armazenados em seus locais anteriores; a chave do registro estará em

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

e o arquivo de cache estará em

`%systemroot%\SchCache`

Nesse caso, as contas de administrador devem executar o aplicativo, o que fará com que o arquivo de esquema seja armazenado em cache no local global para uso futuro pelos usuários menos privilegiados.

 

 