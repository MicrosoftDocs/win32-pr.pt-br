---
description: A função RegOpenUserClassesRoot fornece uma exibição mesclada para processos, como serviços, que estão lidando com clientes diferentes do usuário interativo.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Exibição mesclada de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8597db976922db9ca348488b0092c41ba7c7489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769168"
---
# <a name="merged-view-of-hkey_classes_root"></a>Exibição mesclada da \_ raiz de classes hKey \_

A função [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) fornece uma exibição mesclada para processos, como serviços, que estão lidando com clientes diferentes do usuário interativo. Nesse caso, a chave **de \_ \_ raiz de classes hKey** fornece uma exibição do registro que mescla as informações de **\_ \_ \\ \\ classes de software de computador local hKey** com as informações de **HKEY \_ Current \_ user \\ software \\ classes**.

O sistema usa as seguintes regras para mesclar informações das duas fontes:

-   A exibição mesclada inclui todas as subchaves da chave do **HKEY \_ Current \_ user \\ software \\ classes** .
-   A exibição mesclada inclui todas as subchaves imediatas da chave de **\_ classes de \_ \\ software \\ da máquina local hKey** que não duplicam as subchaves das **\_ classes HKEY Current \_ user \\ software \\**.
-   No final deste tópico há uma lista de subchaves encontradas em **HKEY \_ local \_ Machine \\ software \\ classes** e **HKEY \_ Current \_ user \\ software \\ classes**. As subchaves imediatas dessas chaves da árvore do **\_ \_ computador local hKey** serão incluídas na exibição mesclada somente se não forem duplicatas de subchaves imediatas da árvore de **\_ \_ usuário atual do hKey** . A exibição mesclada não inclui o conteúdo **do \_ \_ computador local hKey** de subchaves duplicadas.

Se um aplicativo for executado com direitos de administrador e o controle de conta de usuário estiver desabilitado, o tempo de execução do COM ignorará a configuração de COM por usuário e acessará apenas a configuração de COM por computador. Os aplicativos que exigem direitos de administrador devem registrar objetos COM dependentes durante a instalação para o repositório de configuração COM por máquina (**HKEY \_ local \_ Machine \\ software \\ classes**). Para obter mais informações, consulte [AC: UAC: configuração de Per-User com](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 e Windows XP/2000:** Os aplicativos podem registrar objetos COM dependentes no repositório de configuração COM por máquina ou por usuário (**HKEY \_ local \_ Machine \\ software \\ classes** ou **HKEY \_ Current \_ user \\ software \\ classes**).

O exemplo a seguir mostra um conjunto de subchaves **no \_ \_ computador local hKey** e o **HKEY \_ Current \_ User** Keys e a exibição mesclada resultante da **\_ \_ raiz de classes hKey**.

**HKEY \_ \_Classes de \\ software \\ de computador local**    **CLSID**       *2*       *4*          **InprocServer32**          **LocalServer32**       *7*

**HKEY \_ \_Classes de \\ software \\ de usuário atuais**    **CLSID**       *1*       *4*          **LocalServer**       *6*       *10*          **LocalServer**

**HKEY \_ CLASSES \_ raiz**    **CLSID**       *1*       *2*       *4*          **InprocServer32**          **LocalServer**          **LocalServer32**       *6*       *7*       *10*          **LocalServer**

As seguintes subchaves são encontradas em **HKEY \_ local \_ Machine \\ software \\ classes** e **HKEY \_ Current \_ user \\ software \\ classes**. Na árvore **do \_ \_ computador local hKey** , as subchaves imediatas dessas chaves serão incluídas na exibição mesclada somente se não forem duplicatas das subchaves imediatas da árvore de **\_ \_ usuário atual do hKey** . A exibição mesclada não inclui o conteúdo **do \_ \_ computador local hKey** de subchaves duplicadas.

**\**_ _*\*\\ shellex**  
**\*\\shellex \\ ContextMenuHandlers**  
**\*\\shellex \\ PropertySheetHandlers**  
**AppID**  
**ClsID**  
**Categorias de componentes**  
**Unidade**  
**Shellex da unidade \\**  
**Unidade \\ shellex \\ ContextMenuHandlers**  
**Unidade \\ shellex \\ PropertySheetHandlers**  
**Talvez**  
**Pasta**  
**Shellex da pasta \\**  
**Pasta \\ shellex \\ ColumnHandler**  
**Pasta \\ shellex \\ ContextMenuHandlers**  
**Pasta \\ shellex \\ ExtShellFolderViews**  
**Pasta \\ shellex \\ PropertySheetHandlers**  
**Componentes do instalador \\**  
**Recursos do instalador \\**  
**Produtos do instalador \\**  
**Interface**  
**MIME**  
**\\Banco de dados MIME**  
**Conjunto de \\ caracteres de banco de dados MIME \\**  
**\\Página de código do banco de dados MIME \\**  
**\\Tipo de conteúdo do banco de dados MIME \\**  
**Importação**  


 

 
