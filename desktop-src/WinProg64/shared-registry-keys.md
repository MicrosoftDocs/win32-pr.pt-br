---
title: Chaves do Registro afetadas pelo WOW64
description: Em WOW64, determinadas chaves do registro são redirecionadas.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- chaves do registro 64-bit Windows programação
- programação de Windows de 64 bits de WOW64, chaves do registro
- chaves do registro redirecionadas 64-bit Windows programação
- chaves do registro refletidas 64-bit Windows programação
- chaves de registro compartilhadas 64-bit Windows programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5193d4aa64848d132aca446c6d1e4a50777614725b69cae637da65aebfe94c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071606"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>chaves do registro afetadas por Windows instalações que incluem Windows no suporte do Windows (WOW) para várias arquiteturas de processador

em Windows de 64 bits instalações que começam com Windows XP e Windows Server 2003 e na arquitetura do processador ARM de 32 bits Windows instalações que começam com Windows RT (Windows 8) (daqui em diante referenciado como **instalações Windowss**), determinadas chaves do registro são *redirecionadas*.

em instalações Windows afetadas, quando um processo com uma arquitetura de processador diferente da arquitetura do processador do sistema operacional (chamado daqui em diante como um **aplicativo WOW**) faz uma chamada do registro para uma chave redirecionada, o redirecionador do registro intercepta a chamada e a mapeia para o local do registro físico correspondente da chave. por exemplo, um aplicativo Intel IA-32 x86 de 32 bits \[  \] em execução em um **AMD64** /intel x86-x64 Windows instalação seria afetado por uma chave de registro redirecionada; quando esse aplicativo x86 chama uma chave redirecionada, o redirecionador do registro intercepta a chamada do aplicativo e redireciona-a para o local do registro físico correspondente da chave. Para obter mais informações, consulte [redirecionador de registro](registry-redirector.md).

outras chaves do registro são *compartilhadas* por aplicativos de diferentes arquiteturas de processador em instalações Windows afetadas. As chamadas de registro de aplicativo WOW para chaves compartilhadas não são redirecionadas. Em vez disso, uma cópia física da chave é mapeada em cada exibição lógica do registro.

**Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Um subconjunto de chaves de registro redirecionadas também é *refletido* para manter as chaves e seus valores sincronizados entre as exibições de 32 bits e 64 bits do registro. a reflexão do registro foi removida a partir do Windows 7 e do Windows Server 2008 R2. Para obter mais informações, consulte [reflexão do registro](registry-reflection.md).

Este tópico lista as chaves do registro que são redirecionadas, compartilhadas ou redirecionadas e refletidas em WOW. ele também lista links simbólicos que fornecem compatibilidade para aplicativos existentes que podem usar caminhos de chave de registro codificados contendo **Wow6432Node**, o local do registro redirecionado para processos x86 em execução em AMD64 Windows instalações. Para saber mais, consulte o seguinte:

- [Chaves redirecionadas, compartilhadas e refletidas sob WOW](#redirected-shared-and-reflected-keys-under-wow)
- [Windows nos Links simbólicos de 64 Windows (WOW64)](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Chaves redirecionadas, compartilhadas e refletidas sob WOW

para aplicativos WOW em instalações Windows afetadas, a tabela a seguir lista as chaves do registro que são redirecionadas, compartilhadas ou redirecionadas e refletidas. As subchaves das chaves nesta tabela herdam o comportamento da chave pai, a menos que especificado de outra forma. Se uma chave não tiver um pai listado nesta tabela, a chave será compartilhada.

| Chave | Windows Server 2008 R2, Windows 7 e mais recente | Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP |
|-|-|-|
| **\_máquina local \_ HKEY** | Compartilhado | Compartilhado |
| **HKEY \_ local \_ MACHINE\SOFTWARE** | Redirected | Redirected |
| **HKEY \_ Classes \_ MACHINE\SOFTWARE locais** \\  | Compartilhado | Redirecionado e refletido |
| **HKEY \_ \_** AppID das \\ **classes** \\  MACHINE\SOFTWARE locais | Compartilhado | Redirecionado e refletido com uma exceção: os valores do registro [DllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) não serão refletidos se seu valor for uma cadeia de caracteres vazia. |
| **HKEY \_ \_** CLSID de \\  \\ **classes** \\  de software de computador local | Redirected | Redirecionado e refletido somente para CLSIDs que não especificam InprocServer32 ou InprocHandler32. |
| **HKEY \_ \_** DirectShow de \\  \\ **Classes** \\  de SOFTWARE de computador LOCAL | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Classes de \\ **software** de computador local \\  \\ **HCP** | Compartilhado | Compartilhado |
| **HKEY \_ \_** Interface de \\  \\ **classes** \\  de software de computador local | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Tipo de \\  \\ **mídia** de classes MACHINE\SOFTWARE locais | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Classes de \\ **software** de computador local \\  \\ **MediaFoundation** | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Clientes de \\ **software** \\  de computador local | Compartilhado | Redirected |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **com3** | Compartilhado | Redirecionado e refletido |
| **HKEY \_ \_Computador local** \\ **software** de \\  \\ **criptografia** \\ **Calais** da Microsoft \\ **atual** | Compartilhado | Compartilhado |
| **HKEY \_ \_Máquina local** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **Calais** \\ **Readers** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE de \_ máquina local** \\  \\  \\  \\ **Serviços** de criptografia da Microsoft | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **CTF** \\ **SystemShared** | Compartilhado | Compartilhado |
| **HKEY \_ \_Máquina local** \\ **software** \\ **Microsoft** \\ **CTF** \\ **Tip** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **DFS** | Compartilhado | Compartilhado |
| **HKEY \_ \_** Assinatura de \\  \\ Driver da **Microsoft do software do** \\  computador local | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **EnterpriseCertificates** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE da \_ máquina local** \\  \\ **Microsoft** \\ **EventSystem** | Compartilhado | Redirecionado e refletido |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **MSMQ** | Compartilhado | Compartilhado |
| **HKEY \_ \_** \\  \\  \\ **Assinatura de não driver** da Microsoft do computador local | Compartilhado | Compartilhado |
| **HKEY \_ \_computador LOCAL** \\ **SOFTWARE** \\ **Microsoft** \\ **Bloco de notas** \\ **defaultfonts** | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **OLE** | Compartilhado | Redirecionado e refletido |
| **HKEY \_ RAS \_ da** Microsoft MACHINE \\ **SOFTWARE** \\  \\ **LOCAL** | Compartilhado | Compartilhado |
| **HKEY \_ RPC \_ da** Microsoft MACHINE \\ **SOFTWARE** \\  \\ **LOCAL** | Compartilhado | Redirecionado e refletido |
| **HKEY \_ SOFTWARE \_ LOCAL** \\ **SOFTWARE** \\ **Microsoft** \\  \\ **Microsoft Microsoft** \\  \\ **MSInfo** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **SystemCertificates** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ LOCAL** \\  \\ **MACHINE Microsoft** \\ **TermServLicensing** | Compartilhado | Compartilhado |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **TransactionServer** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DE COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows** \\ **aplicativo CurrentVersion** \\  | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DE COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **esquemas** \\ **de cursores Painel de Controle** \\ **CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **AutoplayHandlers** | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows** \\  \\  \\ **DriveIcons** do CurrentVersion Explorer | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows** \\ **KindMap do CurrentVersion** \\ **Explorer** \\  | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Política de Grupo** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows** \\ **Políticas currentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows** \\ **Visualização do CurrentVersionHandlers** \\  | Compartilhado | Redirected |
| **HKEY \_ Configuração \_ do** SOFTWARE DO COMPUTADOR LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **locais de telefonia** \\ **CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows NT** \\ **Console CurrentVersion** \\ | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\  \\ **FontDpi** currentVersion | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DE COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **FontLink** \\ **CurrentVersion** | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\  \\ **FontMapper CurrentVersion** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **fontes CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DE COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** Fonte \\ **CurrentVersionSubstitutes** \\  | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ LOCAL** \\ **MACHINE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Gre \_ Initialize** | Compartilhado | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE Microsoft** \\  \\ **Windows NT** opções de execução \\ **de arquivo de imagem CurrentVersion** \\  | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** Pacote de \\ **Idiomas CurrentVersion** \\  | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE \_ DE COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **NetworkCards** \\ **CurrentVersion** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows NT** \\ **portas CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows NT** \\ **CurrentVersion** \\ **Print** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft \\  \\  \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\  \\ **fusos horário** currentversion | Compartilhado | Compartilhado |
| **HKEY \_ Políticas \_ DE** \\ **SOFTWARE DE COMPUTADOR** \\ **LOCAL** | Compartilhado | Compartilhado |
| **HKEY \_ \_** RegisteredApplications de \\ **software** \\  do computador local | Compartilhado | Compartilhado **Windows Server 2003 e Windows XP:** essa chave foi adicionada no Windows Vista. |
| **HKEY \_ Current \_ User** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ usuário atual** \\  | Compartilhado | Compartilhado |
| **HKEY \_ \_** Classes de \\ **software** \\  do usuário atual | Compartilhado | Redirecionado e refletido |
| **HKEY \_ \_** AppID das \\  \\ **classes** \\  de software do usuário atual | Compartilhado | Redirecionado e refletido com uma exceção: os valores do registro [DllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) não serão refletidos se seu valor for uma cadeia de caracteres vazia. |
| **HKEY \_ \_** CLSID de \\  \\ **classes** \\  de software de usuário atual | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** DirectShow de \\  \\ **Classes** \\  de SOFTWARE do usuário atual | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Interface de \\  \\ **classes** \\  de software do usuário atual | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Tipo de \\  \\  \\ **mídia** de classes de software do usuário atual | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Classes de \\ **software** de usuário atuais \\  \\ **MediaFoundation** | Redirected | Redirecionado e refletido |

**HKEY \_ O \_ usuário atual** é um link simbólico para o **\_** SID \\ **\[ \]** de usuários do hKey, onde \[ SID \] indica uma correspondência para a ID de segurança (SID) do usuário atual. **HKEY \_ Os usuários** \\ **\[ SID \]** classes de \\ **software** \\  são um link simbólico para as **\_** \\ **\[ \] \_ classes de Sid** de usuários do HKEY.

**HKEY \_ A \_ raiz de classes** é uma exibição mesclada das classes de software do **\_ \_ computador local hKey** \\  \\  e do **HKEY \_ Current \_ User** \\ **software** \\ . As chaves redirecionadas nesses caminhos de registro são efetivamente redirecionadas para a **\_ \_ raiz de classes hKey** também. Isso também é verdadeiro para chaves refletidas em sistemas que dão suporte a elas.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Windows nos Links simbólicos de 64 Windows (WOW64)

O WOW64 define os seguintes links simbólicos somente para compatibilidade com os aplicativos existentes que podem usar caminhos de chave de registro codificados contendo Wow6432Node. Os novos aplicativos devem evitar o uso de Wow6432Node em caminhos de chave do registro.

- **HKEY \_ As \_ \\ \\ \\ classes Wow6432Node de software do computador local** são vinculadas a **HKEY \_ local \_ Machine \\ software \\ classes \\ Wow6432Node**
- **HKEY \_ As \_ classes de software do computador local \\ \\ \\ Wow6432Node \\ AppID** estão vinculadas ao **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID**
- **HKEY \_ As \_ classes de software da máquina local \\ \\ \\ Wow6432Node \\ protocolos** estão vinculados a **HKEY \_ local \_ Machine \\ software \\ classes \\ protocolos**
- **HKEY \_ \_Classes de software de computador local \\ \\ \\ Wow6432Node \\ TypeLib** está vinculado a **HKEY \_ local \_ Machine \\ software \\ classes \\ TypeLib**

**Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP: HKEY \_ As \_ \\ \\ \\ classes Wow6432Node de software do computador local** são vinculadas a **HKEY \_ local \_ Machine \\ software \\ classes \\ Wow6432Node**. outros links simbólicos foram adicionados no Windows 7 e no Windows Server 2008 R2.
