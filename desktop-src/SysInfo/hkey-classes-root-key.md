---
description: A \_ chave de \_ HKCR (raiz de classes hKey) contém associações de extensão de nome de arquivo e informações de registro de classe com, como ProgIDs, CLSIDs e IIDs. Ele destina-se principalmente à compatibilidade com o registro em Windows de 16 bits.
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: Chave de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca75fc0b736c156e2e0dbe8ad07ff84cbbaa0a9ee1484de74e4f670703b2d875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885678"
---
# <a name="hkey_classes_root-key"></a>Chave de raiz de \_ classes hKey \_

A chave de **HKCR**( **\_ \_ raiz de classes hKey** ) contém associações de extensão de nome de arquivo e informações de registro de classe com, como [ProgIDs](../com/-progid--key.md), [CLSIDs](../com/clsid-key-hklm.md)e [IIDs](../com/interface-key.md). Ele destina-se principalmente à compatibilidade com o registro em Windows de 16 bits.

As informações de registro de classe e extensão de nome de arquivo são armazenadas na **\_ \_ máquina local hKey** e nas chaves de **\_ \_ usuário atuais hKey** . A chave **HKEY \_ local \_ Machine \\ software \\ classes** contém as configurações padrão que podem ser aplicadas a todos os usuários no computador local. A chave **HKEY \_ Current \_ user \\ software \\ classes** contém configurações que se aplicam somente ao usuário interativo. A chave de **\_ \_ raiz de classes hKey** fornece uma exibição do registro que mescla as informações dessas duas fontes. **HKEY \_ A \_ raiz de classes** também fornece essa exibição mesclada para aplicativos projetados para versões anteriores do Windows.

As configurações específicas do usuário têm prioridade sobre as configurações padrão. Por exemplo, a configuração padrão pode especificar um aplicativo específico para manipular .doc arquivos. Mas um usuário pode substituir essa configuração especificando um aplicativo diferente no registro.

Funções de registro como [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) ou [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) permitem que você especifique a chave de **\_ \_ raiz de classes hKey** . Quando você chama essas funções de um processo em execução na conta de usuário interativo, o sistema mescla as configurações padrão em **HKEY \_ local \_ Machine \\ software \\ classes** com as configurações do usuário interativo em **HKEY \_ Current \_ user \\ software \\ classes**. Para obter mais informações sobre como essas configurações são mescladas, consulte [exibição mesclada da \_ \_ raiz de classes hKey](merged-view-of-hkey-classes-root.md).

Para alterar as configurações do usuário interativo, armazene as alterações em **HKEY \_ Current \_ user \\ software \\ classes** , em vez de **HKEY \_ classes \_ root**.

Para alterar as configurações padrão, armazene as alterações em **HKEY \_ local \_ Machine \\ software \\ classes**. Se você gravar chaves em uma chave na **\_ \_ raiz de classes hKey**, o sistema armazenará as informações em **HKEY \_ local \_ Machine \\ software \\ classes**. Se você gravar valores em uma chave na **\_ \_ raiz de classes hKey** e a chave já existir em **HKEY \_ Current \_ user \\ software \\ classes**, o sistema armazenará as informações em vez de em **HKEY \_ local \_ Machine \\ software \\ classes**.

Processos em execução em um contexto de segurança diferente do usuário interativo não devem usar a chave **de \_ \_ raiz de classes hKey** com as funções de registro. Em vez disso, esses processos podem abrir explicitamente a chave do **HKEY \_ local \_ Machine \\ \\ classes de software** para acessar as configurações padrão. Para abrir uma chave do registro que mescla o conteúdo das **\_ classes de \_ \\ software do \\ computador local hKey** com as configurações de um usuário especificado, esses processos podem chamar a função [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) . Por exemplo, um thread que está [representando](/windows/desktop/SecAuthZ/client-impersonation) um cliente pode chamar **RegOpenUserClassesRoot** se precisar recuperar uma exibição mesclada para o cliente que está sendo representado. Observe que o **RegOpenUserClassesRoot** falhará se o perfil do usuário para o usuário especificado não tiver sido carregado. O sistema carrega automaticamente o perfil para o usuário interativo ao fazer logon. Para outros usuários, você precisa chamar a função [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) para carregar explicitamente o perfil do usuário.

Se um aplicativo for executado com direitos de administrador e o controle de conta de usuário estiver desabilitado, o tempo de execução do COM ignorará a configuração COM por usuário e acessará apenas a configuração de COM por máquina. Os aplicativos que exigem direitos de administrador devem registrar objetos COM dependentes durante a instalação para o repositório de configuração COM por máquina (**HKEY \_ local \_ Machine \\ software \\ classes**). Para obter mais informações, consulte [AC: UAC: configuração de Per-User com](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 e Windows XP/2000:** Os aplicativos podem registrar objetos COM dependentes no repositório de configuração COM por máquina ou por usuário (**HKEY \_ local \_ Machine \\ software \\ classes** ou **HKEY \_ Current \_ user \\ software \\ classes**).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\_Classe HKEY classes \_ raiz (referência de registro do kit de recursos)](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
