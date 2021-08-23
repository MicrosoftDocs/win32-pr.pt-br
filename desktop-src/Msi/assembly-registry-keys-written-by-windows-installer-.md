---
description: se um pacote de Windows Installer instalar ou anunciar assemblies, o instalador armazenará informações sobre esses assemblies no registro do sistema local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: chaves do registro de Assembly gravadas por Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fd4a9bf3fa5e1eb557c2a179ec3e9a0853149ff197922a9fbf633a2869f41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746016"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a>chaves do registro de Assembly gravadas por Windows Installer

se um pacote de Windows Installer instalar ou anunciar assemblies, o instalador armazenará informações sobre esses assemblies no registro do sistema local. observe que essas chaves do registro são destinadas apenas para serem usadas internamente pelo Windows Installer e não devem ser contadas de acordo com seu aplicativo. O conteúdo, o local e a estrutura das informações armazenadas nessas chaves estão sujeitos a alterações. Os aplicativos devem depender do [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para gerenciar assemblies.

Os assemblies são registrados por seus nomes de assembly. Os nomes dos valores armazenados nos locais a seguir são os nomes de assembly. Os valores reais são do tipo REG \_ multi \_ sz e contêm dados usados pelo [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) para instalar ou reparar assemblies.

## <a name="information-about-private-assemblies"></a>Informações sobre assemblies privados

Windows o instalador armazena informações sobre assemblies privados transportados por Windows Installer pacotes que foram instalados como aplicativos gerenciados por usuário na seguinte chave do registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Instalador** \\ do **Gerenciado** \\ **SID *_\\_* de usuário** Caminho dos assemblies do instalador para o \\  \\ **_arquivo de configuração_**

Windows o instalador armazena informações sobre assemblies privados transportados por Windows Installer pacotes que foram instalados por usuário na seguinte chave do registro:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Instalador** \\ do **Assemblies** \\ do **_caminho para o arquivo de configuração_**

Windows o instalador armazena informações sobre assemblies privados transportados por pacotes Windows Installer e instalados por computador na seguinte chave do registro:

**HKLM** \\ **Software** \\ **Classes** \\ do **Instalador** \\ do **Assemblies** \\ do **_caminho para o arquivo de configuração_**

## <a name="information-about-global-or-shared-assemblies"></a>Informações sobre assemblies globais ou compartilhados

Windows o instalador armazena informações sobre assemblies compartilhados transportados por Windows Installer pacotes que foram instalados como aplicativos gerenciados por usuário na seguinte chave do registro:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Instalador** \\ do **Gerenciado** \\ **SID *_\\_* de usuário** \\ **Assemblies** do instalador \\ **global**

Windows o instalador armazena informações sobre assemblies compartilhados transportados por Windows Installer pacotes que foram instalados por usuário na seguinte chave do registro:

**HKCU** \\ **Software** \\ **Microsoft** \\ **Instalador** \\ do **Assemblies** \\ do **Global**

Windows o instalador armazena informações sobre assemblies compartilhados transportados por pacotes Windows Installer e instalados por computador na seguinte chave do registro:

**HKLM** \\ **Software** \\ **Classes** \\ do **Instalador** \\ do **Assemblies** \\ do **Global**

 

 



