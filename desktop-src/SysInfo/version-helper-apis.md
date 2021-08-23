---
description: as funções a seguir podem ser usadas para determinar a versão atual do sistema operacional ou identificar se é uma versão Windows ou Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Funções auxiliares de versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7156070e9c793e537d976c82a632142e04cd6669b110b7d0b9fc8da95671b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884167"
---
# <a name="version-helper-functions"></a>Funções auxiliares de versão

as funções a seguir podem ser usadas para determinar a versão atual do sistema operacional ou identificar se é uma versão Windows ou Windows Server. Essas funções fornecem testes simples que usam a função [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) e as comparações recomendadas maiores ou iguais às comparações comprovadas como um meio robusto para determinar a versão do sistema operacional.

> [!Note]  
> essas APIs são definidas por **versionhelpers. h**, que está incluído no Windows 8.1 Software Development Kit (SDK). esse arquivo pode ser usado com outras versões de Microsoft Visual Studio para implementar a mesma funcionalidade para Windows versões anteriores ao Windows 8.1.

<table>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão Windows XP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows XP com Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows XP com Service Pack 2 (SP2).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows XP com Service Pack 3 (SP3).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows Vista.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows Vista com Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows Vista com Service Pack 2 (SP2).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão Windows 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows 7 com Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão Windows 8.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão Windows 8.1.<br/> por Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> retornará false, a menos que o aplicativo contenha um manifesto que inclua uma seção de compatibilidade que contenha os guids que designam Windows 8.1 e/ou Windows 10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>indica se a versão atual do sistema operacional corresponde ou é maior que a versão Windows 10.<br/> por Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> retornará false, a menos que o aplicativo contenha um manifesto que inclua uma seção de compatibilidade que contenha o GUID que designa Windows 10.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></td>
<td>indica se o sistema operacional atual é uma versão de servidor Windows. os aplicativos que precisam distinguir entre as versões de servidor e cliente do Windows devem chamar essa função.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></td>
<td>
<blockquote>Você só deve usar essa função se as outras funções auxiliares de versão fornecidas não se ajustarem ao seu cenário.</blockquote>
<br/>Indica se a versão atual do sistema operacional corresponde ou é maior que as informações de versão fornecidas. essa função é útil na confirmação de uma versão do Windows Server que não compartilha um número de versão com uma versão do cliente.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Exemplo

As funções embutidas definidas no arquivo de cabeçalho **VersionHelpers. h** permitem verificar a versão do sistema operacional retornando um valor **booliano** durante o teste de uma versão do Windows.

por exemplo, se seu aplicativo exigir Windows 8 ou posterior, use o teste a seguir.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Tópicos relacionados

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
