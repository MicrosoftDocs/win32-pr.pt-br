---
description: Lista de recursos protegidos
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Lista de recursos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316a9bf9233283a7c0aba11f0d5fe8a09f38f1e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171808"
---
# <a name="protected-resource-list"></a>Lista de recursos protegidos

Permissão para acesso completo para modificar recursos protegidos por WRP é restrita a TrustedInstaller. Os recursos protegidos por WRP só podem ser alterados usando os [mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md) com o serviço instalador de módulos do Windows.

A WRP protege arquivos com as seguintes extensões instaladas pelo Windows Server 2008 ou Windows Vista:. dll,. exe,. ocx e. sys.

A WRP protege arquivos críticos instalados pelo Windows Server 2008 ou Windows Vista com as seguintes extensões:. ACM,. Ade,. adp,. app,. asa,. asp,. aspx,. AX,. bas,. bat,. bin,. cer,. chm,. CLB,. cmd,. CNT,. CNV,. com,. cpl,. cpx,. CRT,. csh,. dll,. drv,. DTD,. exe,. fxp,. GRP,. H1S,. hlp,. hta,. IME,. inf,. ins,. ISP,. a,. js,. jse,. ksh,. lnk,. Mad,. MAF,. mag ,. Mam,. Man,. maq,. mar,. mas,. enquadrable,. mau,. Mav,. maw,. MDA,. mdb,. mde,. MDT,. mdw,. mdz,. msc,. msi,. msp,. MST,. mui,. NLS,. ocx,. Ops,. PAL,. PCD,. pif,. prf,. prg,. pst,. reg,. scf,. SCR,. SCT,. SHB,. shs,. sys,. tlb,. tsp,. URL,. vb,. vbe,. vbs,. vsmacros,. VSS,. VST,. vsw,. WS,. WSC,. wsf,. WSH,. xsd e. Xsl.

A WRP protege pastas críticas. Uma pasta que contém somente arquivos protegidos por WRP pode ser bloqueada para que apenas o instalador confiável do Windows possa criar arquivos ou subpastas na pasta. Uma pasta pode ser parcialmente bloqueada para permitir que os administradores criem arquivos e subpastas na pasta.

A WRP protege chaves de registro essenciais instaladas pelo Windows Server 2008 e pelo Windows Vista. Se uma chave for protegida por WRP, todas as suas subchaves e valores poderão ser protegidos.

A WRP copia arquivos necessários para reiniciar o Windows no *diretório de cache* localizado em% windir% \\ winsxs \\ backup. Arquivos críticos que não são necessários para reiniciar o Windows não são copiados para o diretório de cache. O tamanho do diretório de cache e a lista de arquivos copiados para o cache não podem ser modificados.

* * Windows Server 2003 e Windows XP: * *

A WFP precedeu a WRP (proteção de arquivo do Windows).

A WFP protege os arquivos instalados pelo Windows com as seguintes extensões:. dll,. exe,. ocx e. sys. Além disso, as fontes TrueType Micross. ttf, Tahoma. ttf e tahomabd. ttf também são protegidas.

No final da instalação do Windows, a WFP executa uma verificação de todos os arquivos protegidos para garantir que eles não tenham sido modificados por aplicativos instalados por meio da instalação autônoma. A WFP também copia versões verificadas desses arquivos de sistema para o diretório de cache. Quando um aplicativo tenta substituir um arquivo protegido, a WFP pode restaurar o arquivo original do diretório de cache.

O valor padrão é% SystemRoot% \\ System32 \\ dllcache. Para especificar um local diferente para o cache, crie o seguinte valor de registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Esse deve ser um caminho local. O uso de um caminho de rede cria uma única fonte de rede compartilhada para arquivos de cache, desde que todos os clientes que usam o compartilhamento estejam executando os mesmos service packs e hotfixes.

O tamanho padrão do cache é ilimitado. Para alterar o tamanho do cache, use a seguinte configuração do registro: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Se o valor for SFC \_ quota \_ todos os \_ arquivos, todos os arquivos do sistema serão armazenados em cache no diretório de cache.

Devido a considerações de espaço em disco, talvez não seja desejável manter versões em cache de todos os arquivos do sistema no diretório de cache. Dependendo do tamanho do cache, a WFP armazenará as versões de arquivo verificadas no diretório de cache do disco rígido do sistema. A WFP adicionará arquivos ao cache até que o tamanho do diretório de cache atinja o limite especificado.

Quando um aplicativo tenta substituir um arquivo protegido que não está no cache, a WFP tenta restaurar o arquivo original da origem de instalação, solicitando o usuário, se necessário.

 

 



