---
description: Lista de recursos protegidos
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Lista de recursos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c221068d9185c289d601f53c6b76df9677d8bc213b44f3dc13dbf5b66a0df446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760116"
---
# <a name="protected-resource-list"></a>Lista de recursos protegidos

Permissão para acesso completo para modificar recursos protegidos por WRP é restrita a TrustedInstaller. os recursos protegidos por WRP só podem ser alterados usando os [mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md) com o serviço instalador de módulos Windows.

a WRP protege arquivos com as seguintes extensões instaladas pelo Windows Server 2008 ou Windows Vista: .dll, .exe,. ocx e .sys.

a WRP protege arquivos críticos que são instalados pelo Windows Server 2008 ou Windows Vista com as seguintes extensões:. acm,. ade,. adp,. app,. asa,. asp,. aspx,. ax,. bas, .bat,. bin,. cer,. chm,. clb,. cmd,. cnt,. cnv,. com, .cpl,. cpx,. crt,. csh, .dll,. drv,. dtd, .exe,. fxp,. grp,. h1s,. hlp,. hta,. ime,. inf,. ins,. isp,. a, .js,. jse,. ksh,. lnk,. mad,. maf,. mag,. mam,. man,. maq,. mar,. mas,. passe-os,. mau,. mav,. maw,. mda,. mdb,. mde,. mdt,. mdw,. mdz,. msc, .msi,. msp,. mst,. mui,. nls,. ocx,. ops,. pal,. pcd,. pif,. prf,. prg,. pst,. reg,. scf,. scr,. sct,. shb,. shs, .sys,. tlb,. tsp,. url,. vb,. vbe,. vbs,. vsmacros,. vss,. vst,. vsw,. ws,. wsc,. wsf,. wsh,  . xsd e. Xsl.

A WRP protege pastas críticas. uma pasta que contém somente arquivos protegidos por WRP pode ser bloqueada para que apenas o Windows instalador confiável possa criar arquivos ou subpastas na pasta. Uma pasta pode ser parcialmente bloqueada para permitir que os administradores criem arquivos e subpastas na pasta.

a WRP protege chaves de registro essenciais instaladas pelo Windows Server 2008 e Windows Vista. Se uma chave for protegida por WRP, todas as suas subchaves e valores poderão ser protegidos.

a WRP copia os arquivos necessários para reiniciar Windows no *diretório de cache* localizado em% Windir% \\ winsxs \\ Backup. os arquivos críticos que não são necessários para reiniciar Windows não são copiados para o diretório de cache. O tamanho do diretório de cache e a lista de arquivos copiados para o cache não podem ser modificados.

* * Windows Server 2003 e Windows XP: * *

Windows Proteção de arquivo (WFP) precedida por WRP.

a WFP protege os arquivos instalados pelo Windows com as seguintes extensões: .dll, .exe,. ocx e .sys. Além disso, as fontes TrueType Micross. ttf, Tahoma. ttf e tahomabd. ttf também são protegidas.

no final da instalação do Windows, a WFP executa uma verificação de todos os arquivos protegidos para garantir que eles não tenham sido modificados por aplicativos instalados por meio da instalação autônoma. A WFP também copia versões verificadas desses arquivos de sistema para o diretório de cache. Quando um aplicativo tenta substituir um arquivo protegido, a WFP pode restaurar o arquivo original do diretório de cache.

O valor padrão é% SystemRoot% \\ System32 \\ dllcache. para especificar um local diferente para o cache, crie o seguinte valor de registro: **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Esse deve ser um caminho local. O uso de um caminho de rede cria uma única fonte de rede compartilhada para arquivos de cache, desde que todos os clientes que usam o compartilhamento estejam executando os mesmos service packs e hotfixes.

O tamanho padrão do cache é ilimitado. para alterar o tamanho do cache, use a seguinte configuração do registro: **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Se o valor for SFC \_ quota \_ todos os \_ arquivos, todos os arquivos do sistema serão armazenados em cache no diretório de cache.

Devido a considerações de espaço em disco, talvez não seja desejável manter versões em cache de todos os arquivos do sistema no diretório de cache. Dependendo do tamanho do cache, a WFP armazenará as versões de arquivo verificadas no diretório de cache do disco rígido do sistema. A WFP adicionará arquivos ao cache até que o tamanho do diretório de cache atinja o limite especificado.

Quando um aplicativo tenta substituir um arquivo protegido que não está no cache, a WFP tenta restaurar o arquivo original da origem de instalação, solicitando o usuário, se necessário.

 

 



