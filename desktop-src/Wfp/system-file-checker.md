---
description: O utilitário do verificador de arquivos do sistema, Sfc.exe, permite que os administradores verifiquem todos os recursos protegidos para verificar suas versões.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: " Verificador de Arquivos do Sistema"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757057"
---
# <a name="system-file-checker"></a> Verificador de Arquivos do Sistema

O utilitário do verificador de arquivos do sistema, Sfc.exe, permite que os administradores verifiquem todos os recursos protegidos para verificar suas versões.

Arquivos críticos para reiniciar o Windows que não correspondem à versão esperada do Windows podem ser substituídos pelas versões corretas. Se um arquivo for reparado, os dados de registro correspondentes também serão reparados. Arquivos protegidos não críticos para reiniciar o Windows não são reparados.

## <a name="syntax"></a>Syntax

A seguir está a sintaxe de linha de comando para o Sfc.

**Opções de SFC \[ = caminho completo do arquivo\]**

## <a name="options"></a>Opções

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*
</dt> <dd>

Não há suporte para esse valor.

**Windows Server 2003 e Windows XP:** Define o tamanho do cache de arquivos. O tamanho padrão do cache é 0x32 (50 MB).

</dd> <dt>

<span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL
</dt> <dd>

Não há suporte para esse valor.

</dd> <dt>

<span id="_ENABLE"></span><span id="_enable"></span>/ENABLE
</dt> <dd>

Não há suporte para esse valor.

</dd> <dt>

<span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY
</dt> <dd>

Verificar ou reparar somente arquivos. Não verifique ou repare as chaves do registro.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Use esta opção para reparos offline. Especifique o local do diretório de inicialização offline.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Use esta opção para reparos offline. Especifique o local do diretório offline do Windows.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Não há suporte para esse valor.

**Windows Server 2003 e Windows XP:** Esvazia o cache de arquivos e examina todos os arquivos protegidos do sistema.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/QUIET
</dt> <dd>

Não há suporte para esse valor.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

Retornar às configurações padrão.

**Windows Server 2008 e Windows Vista:** Sem suporte.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT
</dt> <dd>

Não há suporte para esse valor.

**Windows Server 2003 e Windows XP:** Examina todos os arquivos protegidos do sistema em cada inicialização.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

Verifica e repara o arquivo localizado no caminho completo especificado.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW
</dt> <dd>

Examina todos os arquivos protegidos do sistema imediatamente.

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE
</dt> <dd>

Não há suporte para esse valor.

**Windows Server 2003 e Windows XP:** Examina todos os arquivos protegidos do sistema na próxima inicialização.

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE
</dt> <dd>

Verifica o arquivo no caminho completo especificado. Essa opção não repara o arquivo.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

Examina todos os arquivos protegidos do sistema, mas não repara os arquivos.

**Windows XP:** Sem suporte.

</dd> </dl>

O SFC define o seguinte valor de registro:

 = HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCScan

Para obter mais informações, consulte [valores do registro de WFP](wfp-registry-values.md).

## <a name="remarks"></a>Comentários

Somente no Windows Vista, você pode definir a variável de ambiente do arquivo de **\_ \_ log do Windows TRACING** para o local de um diretório válido para receber um arquivo de log.

## <a name="examples"></a>Exemplos

As linhas de comando de exemplo a seguir são exemplos de sintaxe de sfc.exe.

**SFC/SCANNOW**

**Sfc/VERIFYFILE = c: \\ Windows \\ System32 \\kernel32.dll**

**Sfc/SCANFILE = d: \\ Windows \\ System32 \\kernel32.dll/OFFBOOTDIR = d: \\ /OFFWINDIR = d: \\ Windows**

**/FILESONLY/VERIFYONLY Sfc**

 

 



