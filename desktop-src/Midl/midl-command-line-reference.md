---
title: Referência de Command-Line de MIDL
description: Esta seção contém informações de referência para cada opção de linha de comando e opções de comutador reconhecidas pelo compilador Microsoft RPC MIDL.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- MIDL linguagem IDL da Microsoft, referência
- MIDL de referência de linha de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df927ded3f1a46045437fe1f9e72e2c7f80dd17d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887342"
---
# <a name="midl-command-line-reference"></a>Referência de Command-Line de MIDL

Esta seção contém informações de referência para cada opção de linha de comando e opções de comutador reconhecidas pelo compilador Microsoft RPC MIDL. As entradas de comutador são organizadas em ordem alfabética. A [sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md) descreve a sintaxe de linha de comando geral.

<dl>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)  
[O comando arquivo de resposta](the-response-file-command.md)  
[**/acf**](-acf.md)  
[**/align**](-align.md)  
[**/amd64**](-amd64.md)  
[**configuração do/App \_**](-app-config.md)  
[compatível com/Backward \_](-backward-compat.md)  
[**/c \_ ext**](-c-ext.md)  
[**/caux**](-caux.md)  
[**/Char**](-char.md)  
[**/Client**](-client.md)  
[**/confirm**](-confirm.md)  
[**/cpp \_ cmd**](-cpp-cmd.md)  
[**/cpp \_ aceitar**](-cpp-opt.md)  
[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)  
[**/D**](-d.md)  
[**/dlldata nomedearquivo**](-dlldata.md)  
[**/env**](-env.md)  
[**/Error**](-error.md)  
[**/Error**](-error.md)  
[**/h**](-h.md)  
[**/header**](-header.md)  
[**/Help (/?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/IID nomedearquivo**](-iid.md)  
[**/Import**](-import.md)  
[**/LCID**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**/MS \_ ext**](-ms-ext.md)  
[**/MS \_ Union**](-ms-union.md)  
[**/MSC \_ Ver**](-msc-ver.md)  
[**/new**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/// \_ /nocpp**](-no-cpp-nocpp.md)  
[**/ \_ \_ EPV padrão**](-no-default-epv.md)  
[**/. de \_ \_ Idir def**](-no-def-idir.md)  
[**\_opção de formato de/// \_**](-no-format-opt.md)  
[**// \_ avançado**](-no-robust.md)  
[**// \_ avisar**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/Oi**](-oi.md)  
[**/old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/Os**](-os.md)  
[**/osf**](-osf.md)  
[**/out**](-out.md)  
[**/Pack**](-pack.md)  
[**/prefix**](-prefix.md)  
[**/protocol**](-protocol.md)  
[**/proxy nomedearquivo**](-proxy.md)  
[**/robust**](-robust.md)  
[**/rpcss**](-rpcss.md)  
[**/sal**](-sal.md)  
[**/sal \_ local**](-sal-local.md)  
[**/saux**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**verificação de/Syntax \_**](-syntax-check.md)  
[**/&lt;sistema&gt;**](-system-.md)  
[**/debug**](-target.md)  
[**/tlb**](-tlb.md)  
[**/U**](-u.md)  
[**/Use \_ EPV**](-use-epv.md)  
[**/Version \_ carimbo**](-version-stamp.md)  
[**/W**](-w.md)  
[**/Warn**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/ZP**](-zp.md)  
[**/ZS**](-zs.md)  
</dl>

O compilador MIDL pode gerar código para diferentes plataformas e versões do sistema. Consulte a opção [**/target**](-target.md) para saber mais sobre as opções sugeridas e como gerar código otimizado para uma determinada versão.

Observe que o sinal de subtração (–) pode ser substituído pela barra (/) em todas as opções de linha de comando MIDL que começam com uma barra (/). O exemplo a seguir demonstra sua equivalência ao invocar o compilador MIDL.

## <a name="examples"></a>Exemplos

**MIDL/ACF meu nome de arquivo \_ ACF. ACF** ** * *. idl**

**MIDL-ACF My \_ ACF. ACF** *filename * * *. idl**

 

 




