---
description: A função RegOpenUserClassesRoot fornece uma exibição mesclada para processos, como serviços, que estão lidando com clientes diferentes do usuário interativo.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Exibição mesclada de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52b48be32ec524cdac42808d7f4efddfc78854b56133e647d6f5a9b06ae88bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885408"
---
# <a name="merged-view-of-hkey_classes_root"></a>Exibição mesclada de CLASSES HKEY \_ \_ ROOT

A [**função RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) fornece uma exibição mesclada para processos, como serviços, que estão lidando com clientes diferentes do usuário interativo. Nesse caso, a chave RAIZ **de CLASSES HKEY \_ \_** fornece uma exibição do Registro que mescla as informações das Classes de Software HKEY LOCAL MACHINE com as informações de Classes de **\_ \_ \\ \\ Software HKEY** **CURRENT \_ \_ USER \\ \\**.

O sistema usa as seguintes regras para mesclar informações das duas fontes:

-   A exibição mesclada inclui todas as sub-chaves da chave **HKEY \_ CURRENT USER \_ Software \\ \\ Classes.**
-   A exibição mesclada inclui todas as sub-chaves imediatas da chave classes de software HKEY LOCAL MACHINE que não duplicam as sub-chaves das Classes de **\_ \_ \\ \\ Software** do USUÁRIO ATUAL do **HKEY. \_ \_ \\ \\**
-   No final deste tópico, há uma lista de sub-chaves encontradas em Classes de **Software HKEY \_ LOCAL \_ MACHINE \\ \\** e **HKEY CURRENT USER Software \_ \_ \\ \\ Classes**. As sub-chaves imediatas dessas chaves da árvore **HKEY \_ LOCAL \_ MACHINE** serão incluídas na exibição mesclada somente se não são duplicatas de sub-chaves imediatas da árvore **HKEY \_ CURRENT \_ USER.** A exibição mesclada não inclui o conteúdo **de HKEY \_ LOCAL \_ MACHINE** de subkeys duplicadas.

Se um aplicativo for executado com direitos de administrador e o Controle de Conta de Usuário estiver desabilitado, o runtime COM ignorará a configuração COM por usuário e acessará apenas a configuração COM por computador. Os aplicativos que exigem direitos de administrador devem registrar objetos COM dependentes durante a instalação no armazenamento de configuração COM por computador ( Classes de **software HKEY \_ LOCAL \_ MACHINE \\ \\**). Para obter mais informações, [consulte AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 e Windows XP/2000:** Os aplicativos podem registrar objetos COM dependentes no armazenamento de configuração COM por computador ou por usuário ( Classes de software HKEY LOCAL MACHINE ou classes de **\_ \_ \\ \\** software do usuário atual **\_ \_ \\ \\ HKEY).**

O exemplo a seguir mostra um conjunto de sub-chaves nas chaves **HKEY \_ LOCAL \_ MACHINE** e **HKEY \_ CURRENT \_ USER** e a exibição mesclada resultante de **HKEY CLASSES \_ \_ ROOT.**

**HKEY \_ CLASSES \_ DE \\ SOFTWARE \\ DE** COMPUTADOR LOCAL **CLSID***2**4***inprocserver32****localserver32***7*                                             

**HKEY \_ CLASSES \_ DE \\ Software \\ DO**    **USUÁRIO ATUAL CLSID**       *1*       *4*          **localserver**       *6*       *10*          **localserver**

**HKEY \_ CLASSES \_ ROOT****CLSID***1**2**4***inprocserver32****localserver localserver32***6**7**10***localserver**                                                                                      

As sub-chaves a seguir são encontradas em Classes de **Software HKEY \_ LOCAL MACHINE \_ \\ \\ e** **HKEY CURRENT USER Software \_ \_ \\ \\ Classes**. Na árvore **HKEY \_ LOCAL \_ MACHINE,** as sub-chaves imediatas dessas chaves serão incluídas na exibição mesclada somente se não são duplicatas de subkeys imediatas da árvore **HKEY \_ CURRENT \_ USER.** A exibição mesclada não inclui o conteúdo **de HKEY \_ LOCAL \_ MACHINE** de subkeys duplicadas.

**\***  
**\*\\shellex**  
**\*\\Shellex \\ ContextMenuHandlers**  
**\*\\Shellex \\ PropertySheetHandlers**  
**AppID**  
**Clsid**  
**Categorias de componentes**  
**Unidade**  
**Shellex \\ de unidade**  
**\\ \\ ContextMenuHandlers do shellex de unidade**  
**\\ \\ PropertySheetHandlers do shellex da unidade**  
**FileType**  
**Pasta**  
**Shellex \\ de pasta**  
**\\ColumnHandler do \\ shellex da pasta**  
**\\ContextMenuHandlers do shellex \\ de pasta**  
**Shell \\ de \\ pastaEx ExtShellFolderViews**  
**\\PropertySheetHandlers do shellex \\ da pasta**  
**Componentes do \\ instalador**  
**Recursos do \\ instalador**  
**Produtos do \\ instalador**  
**Interface**  
**Mime**  
**Banco de dados Mime \\**  
**Mime \\ Database \\ Charset**  
**Página de código \\ do banco de dados \\ mime**  
**Tipo de conteúdo \\ do banco de dados Mime \\**  
**Typelib**  


 

 
