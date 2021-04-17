---
title: Chaves do Registro afetadas pelo WOW64
description: Em WOW64, determinadas chaves do registro são redirecionadas.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- chaves do registro programação de 64 bits do Windows
- Programação WOW64 de 64 bits do Windows, chaves do registro
- chaves do registro redirecionadas-programação do Windows de 64 bits
- chaves do registro refletidas, programação do Windows de 64 bits
- chaves do registro compartilhado 64-programação do Windows-bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48278bfd42656b05d0e1f2be4402496a873022d1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "105768373"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>Chaves do registro afetadas por instalações do Windows que incluem o suporte do Windows no Windows (WOW) para várias arquiteturas de processador

Em instalações do Windows de 64 bits que começam com o Windows XP e o Windows Server 2003 e na arquitetura do processador do ARM de 32 bits instalações do Windows a partir do Windows RT (Windows 8) (daqui em diante referenciadas como **instalações afetadas do Windows**), determinadas chaves do registro são *redirecionadas*.

Em instalações afetadas do Windows, quando um processo com uma arquitetura de processador diferente da arquitetura do processador do sistema operacional (chamado daqui em diante como um **aplicativo wow**) faz uma chamada do registro para uma chave redirecionada, o redirecionador do registro intercepta a chamada e a mapeia para o local do registro físico correspondente da chave. Por exemplo, um aplicativo Intel IA-32 x86 de 32 bits \[  \] em execução em uma instalação **AMD64** /Intel x86-x64 do Windows seria afetado por uma chave de registro redirecionada; quando esse aplicativo x86 chama uma chave redirecionada, o redirecionador do registro intercepta a chamada do aplicativo e redireciona-a para o local do registro físico correspondente da chave. Para obter mais informações, consulte [redirecionador de registro](registry-redirector.md).

Outras chaves do registro são *compartilhadas* por aplicativos de diferentes arquiteturas de processador em instalações afetadas do Windows. As chamadas de registro de aplicativo WOW para chaves compartilhadas não são redirecionadas. Em vez disso, uma cópia física da chave é mapeada em cada exibição lógica do registro.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Um subconjunto de chaves de registro redirecionadas também é *refletido* para manter as chaves e seus valores sincronizados entre as exibições de 32 bits e 64 bits do registro. A reflexão do registro foi removida a partir do Windows 7 e do Windows Server 2008 R2. Para obter mais informações, consulte [reflexão do registro](registry-reflection.md).

Este tópico lista as chaves do registro que são redirecionadas, compartilhadas ou redirecionadas e refletidas em WOW. Ele também lista links simbólicos que fornecem compatibilidade para aplicativos existentes que podem usar caminhos de chave de registro codificados contendo **Wow6432Node**, o local do registro Redirecionado para processos x86 em execução em instalações do Windows do AMD64. Para saber mais, consulte o seguinte:

- [Chaves redirecionadas, compartilhadas e refletidas sob WOW](#redirected-shared-and-reflected-keys-under-wow)
- [Links simbólicos do Windows no Windows 64 (WOW64)](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Chaves redirecionadas, compartilhadas e refletidas sob WOW

Para aplicativos WOW em instalações afetadas do Windows, a tabela a seguir lista as chaves do registro que são redirecionadas, compartilhadas ou redirecionadas e refletidas. As subchaves das chaves nesta tabela herdam o comportamento da chave pai, a menos que especificado de outra forma. Se uma chave não tiver um pai listado nesta tabela, a chave será compartilhada.

| Chave | Windows Server 2008 R2, Windows 7 e mais recente | Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP |
|-|-|-|
| **\_máquina local \_ HKEY** | Compartilhado | Compartilhado |
| **HKEY \_ local \_ MACHINE\SOFTWARE** | Redirected | Redirected |
| **HKEY \_ Classes \_ MACHINE\SOFTWARE locais** \\  | Compartilhado | Redirecionado e refletido |
| **HKEY \_ \_** AppID das \\ **classes** \\  MACHINE\SOFTWARE locais | Compartilhado | Redirecionado e refletido com uma exceção: os valores do registro [DllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) não serão refletidos se seu valor for uma cadeia de caracteres vazia. |
| **HKEY \_ \_** CLSID de \\  \\ **classes** \\  de software de computador local | Redirected | Redirecionado e refletido somente para CLSIDs que não especificam InprocServer32 ou InprocHandler32. |
| **HKEY \_ \_** Classes de \\ **software** do computador local \\  \\ **DirectShow** | Redirected | Redirecionado e refletido |
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
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **bloco de notas** \\ **fonts** | Compartilhado | Redirected |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **OLE** | Compartilhado | Redirecionado e refletido |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **RAS** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **RPC** | Compartilhado | Redirecionado e refletido |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\  \\  \\ **ferramentas compartilhadas** Microsoft \\ **MSInfo** | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **SystemCertificates** | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **TermServLicensing** | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **TransactionServer** | Compartilhado | Compartilhado |
| **HKEY \_ \_** Caminhos de \\  \\ **aplicativo do Microsoft** \\ **Windows** \\ **CurrentVersion** \\  do computador local software | Compartilhado | Redirected |
| **HKEY \_ \_** Esquemas de \\  \\  \\  \\  \\  \\ **cursores** \\  do painel de controle do software do computador local Microsoft Windows CurrentVersion | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **AutoplayHandlers** | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **DriveIcons** | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **KindMap** | Compartilhado | Redirected |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **política de grupo** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **políticas do Microsoft** \\ **Windows** \\ **CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | Compartilhado | Redirected |
| **HKEY \_ \_** \\  \\ Instalação do software do computador local **Microsoft** \\ **Windows** \\ **CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ \_** Locais de \\  \\  \\  \\  \\ **telefonia** \\  do software do computador local Microsoft Windows CurrentVersion | Compartilhado | Compartilhado |
| **HKEY \_ Console do \_ computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ | Compartilhado | Redirected |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontDpi** | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontLink** | Compartilhado | Redirected |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontMapper** | Compartilhado | Compartilhado |
| **HKEY \_ \_** Fontes de \\ **software** do computador local \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **fonts** | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontSubstitutes** | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **GRE \_ Initialize** | Compartilhado | Redirected |
| **HKEY \_ \_** Opções de \\  \\ execução **do** arquivo de imagem do software do computador local Microsoft \\ **Windows NT** \\ **CurrentVersion** \\  | Compartilhado | Redirected |
| **HKEY \_ \_** Pacote de \\  \\ idiomas do software do computador local Microsoft \\ **Windows NT** \\ **CurrentVersion** \\  | Compartilhado | Redirected |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **NetworkCards** | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Compartilhado | Compartilhado |
| **HKEY \_ \_Computador local** \\ **software** \\ **portas Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ \_** \\  \\ Impressão do software do computador local **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\  | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ computador local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Time Zones** | Compartilhado | Compartilhado |
| **HKEY \_ \_** Políticas de \\ **software** \\  de computador local | Compartilhado | Compartilhado |
| **HKEY \_ \_** RegisteredApplications de \\ **software** \\  do computador local | Compartilhado | Compartilhado **Windows Server 2003 e Windows XP:** Essa chave foi adicionada ao Windows Vista. |
| **HKEY \_ Current \_ User** | Compartilhado | Compartilhado |
| **HKEY \_ SOFTWARE do \_ usuário atual** \\  | Compartilhado | Compartilhado |
| **HKEY \_ \_** Classes de \\ **software** \\  do usuário atual | Compartilhado | Redirecionado e refletido |
| **HKEY \_ \_** AppID das \\  \\ **classes** \\  de software do usuário atual | Compartilhado | Redirecionado e refletido com uma exceção: os valores do registro [DllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) não serão refletidos se seu valor for uma cadeia de caracteres vazia. |
| **HKEY \_ \_** CLSID de \\  \\ **classes** \\  de software de usuário atual | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Classes de \\ **software** de usuário atuais \\  \\ **DirectShow** | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Interface de \\  \\ **classes** \\  de software do usuário atual | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Tipo de \\  \\  \\ **mídia** de classes de software do usuário atual | Redirected | Redirecionado e refletido |
| **HKEY \_ \_** Classes de \\ **software** de usuário atuais \\  \\ **MediaFoundation** | Redirected | Redirecionado e refletido |

**HKEY \_ O \_ usuário atual** é um link simbólico para o **\_** SID \\ **\[ \]** de usuários do hKey, onde \[ SID \] indica uma correspondência para a ID de segurança (SID) do usuário atual. **HKEY \_ Os usuários** \\ **\[ SID \]** classes de \\ **software** \\  são um link simbólico para as **\_** \\ **\[ \] \_ classes de Sid** de usuários do HKEY.

**HKEY \_ A \_ raiz de classes** é uma exibição mesclada das classes de software do **\_ \_ computador local hKey** \\  \\  e do **HKEY \_ Current \_ User** \\ **software** \\ . As chaves redirecionadas nesses caminhos de registro são efetivamente redirecionadas para a **\_ \_ raiz de classes hKey** também. Isso também é verdadeiro para chaves refletidas em sistemas que dão suporte a elas.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Links simbólicos do Windows no Windows 64 (WOW64)

O WOW64 define os seguintes links simbólicos somente para compatibilidade com os aplicativos existentes que podem usar caminhos de chave de registro codificados contendo Wow6432Node. Os novos aplicativos devem evitar o uso de Wow6432Node em caminhos de chave do registro.

- **HKEY \_ As \_ \\ \\ \\ classes Wow6432Node de software do computador local** são vinculadas a **HKEY \_ local \_ Machine \\ software \\ classes \\ Wow6432Node**
- **HKEY \_ As \_ classes de software do computador local \\ \\ \\ Wow6432Node \\ AppID** estão vinculadas ao **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID**
- **HKEY \_ As \_ classes de software da máquina local \\ \\ \\ Wow6432Node \\ protocolos** estão vinculados a **HKEY \_ local \_ Machine \\ software \\ classes \\ protocolos**
- **HKEY \_ \_Classes de software de computador local \\ \\ \\ Wow6432Node \\ TypeLib** está vinculado a **HKEY \_ local \_ Machine \\ software \\ classes \\ TypeLib**

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP: hKey \_ As \_ \\ \\ \\ classes Wow6432Node de software do computador local** são vinculadas a **HKEY \_ local \_ Machine \\ software \\ classes \\ Wow6432Node**. Outros links simbólicos foram adicionados ao Windows 7 e ao Windows Server 2008 R2.
