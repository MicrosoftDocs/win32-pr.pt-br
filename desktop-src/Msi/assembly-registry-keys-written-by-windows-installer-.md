---
description: Se um pacote de Windows Installer instalar ou anunciar assemblies, o instalador armazenará informações sobre esses assemblies no registro do sistema local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Chaves do registro de assembly gravadas por Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505799"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>Chaves do registro de assembly gravadas por Windows Installer

Se um pacote de Windows Installer instalar ou anunciar assemblies, o instalador armazenará informações sobre esses assemblies no registro do sistema local. Observe que essas chaves do registro são destinadas apenas para serem usadas internamente pelo Windows Installer e não devem ser contadas de acordo com seu aplicativo. O conteúdo, o local e a estrutura das informações armazenadas nessas chaves estão sujeitos a alterações. Os aplicativos devem depender do [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para gerenciar assemblies.

Os assemblies são registrados por seus nomes de assembly. Os nomes dos valores armazenados nos locais a seguir são os nomes de assembly. Os valores reais são do tipo REG \_ multi \_ sz e contêm dados usados pelo [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para instalar ou reparar assemblies.

## <a name="information-about-private-assemblies"></a>Informações sobre assemblies privados

Windows Installer armazena informações sobre assemblies privados transmitidos por Windows Installer pacotes que foram instalados como aplicativos gerenciados por usuário na seguinte chave do registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Instalador** \\ do **Gerenciado** \\ **SID *_\\_* de usuário** Caminho dos assemblies do instalador para o \\  \\ * *_arquivo de configuração_* _

Windows Installer armazena informações sobre assemblies privados transmitidos por Windows Installer pacotes que foram instalados por usuário na seguinte chave do registro:

_*HKCU **\\** software **\\** Microsoft **\\** Installer **\\** assemblies **\\** _caminho para o arquivo de configuração_*_

Windows Installer armazena informações sobre assemblies privados transportados por pacotes Windows Installer e instalados por computador na seguinte chave do registro:

_*HKLM **\\** o **\\** caminho dos assemblies do **\\** instalador **\\** de classes de software para o **\\** _arquivo de configuração_*_

## <a name="information-about-global-or-shared-assemblies"></a>Informações sobre assemblies globais ou compartilhados

Windows Installer armazena informações sobre assemblies compartilhados transmitidos por Windows Installer pacotes que foram instalados como aplicativos gerenciados por usuário na seguinte chave do registro:

_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\** _User Sid_*_ \\ _ *Installer **\\** assemblies **\\** global**

Windows Installer armazena informações sobre assemblies compartilhados transmitidos por Windows Installer pacotes que foram instalados por usuário na seguinte chave do registro:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Instalador** \\ do **Assemblies** \\ do **Global**

Windows Installer armazena informações sobre assemblies compartilhados transmitidos por Windows Installer pacotes e instalados por computador na seguinte chave do registro:

**HKLM** \\ **Software** \\ **Classes** \\ do **Instalador** \\ do **Assemblies** \\ do **Global**

 

 



