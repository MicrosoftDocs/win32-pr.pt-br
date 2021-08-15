---
description: O utilitário do verificador de arquivos do sistema, Sfc.exe, permite que os administradores verifiquem todos os recursos protegidos para verificar suas versões.
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: " Verificador de Arquivos do Sistema"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f751aa30c06dbff90b8d5221974236b45edf9f0f278c144f755568a0040f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330278"
---
# <a name="system-file-checker"></a> Verificador de Arquivos do Sistema

O utilitário do verificador de arquivos do sistema, Sfc.exe, permite que os administradores verifiquem todos os recursos protegidos para verificar suas versões.

Arquivos críticos para reiniciar Windows que não corresponderem à versão Windows esperada podem ser substituídos por versões corretas. Se um arquivo for reparado, os dados do Registro correspondentes também serão reparados. Arquivos protegidos não críticos para reiniciar Windows não são reparados.

## <a name="syntax"></a>Syntax

A seguir está a sintaxe de linha de comando para Sfc.

**Opções de SFC \[ =caminho de arquivo completo\]**

## <a name="options"></a>Opções

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE=*x*
</dt> <dd>

Não há suporte para esse valor.

**Windows Server 2003 e Windows XP:** Define o tamanho do cache de arquivo. O tamanho padrão do cache é 0x32 (50 MB).

</dd> <dt>

<span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL
</dt> <dd>

Não há suporte para esse valor.

</dd> <dt>

<span id="_ENABLE"></span><span id="_enable"></span>/enable
</dt> <dd>

Não há suporte para esse valor.

</dd> <dt>

<span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY
</dt> <dd>

Verifique ou repare apenas arquivos. Não verifique nem repare as chaves do Registro.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

Use essa opção para reparos offline. Especifique o local do diretório de inicialização offline.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

Use essa opção para reparos offline. Especifique o local do diretório Windows offline.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

Não há suporte para esse valor.

**Windows Server 2003 e Windows XP:** Esvazia o cache de arquivos e examina todos os arquivos do sistema protegidos.

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/quiet
</dt> <dd>

Não há suporte para esse valor.

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

Retorne às configurações padrão.

**Windows Server 2008 e Windows Vista:** Sem suporte.

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT
</dt> <dd>

Não há suporte para esse valor.

**Windows Server 2003 e Windows XP:** Examina todos os arquivos do sistema protegidos em cada inicialização.

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

Examina e repara o arquivo localizado no caminho completo especificado.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW
</dt> <dd>

Examina todos os arquivos do sistema protegidos imediatamente.

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/S LTDANCE
</dt> <dd>

Não há suporte para esse valor.

**Windows Server 2003 e Windows XP:** Examina todos os arquivos do sistema protegidos na próxima inicialização.

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE
</dt> <dd>

Verifica o arquivo no caminho completo especificado. Essa opção não repara o arquivo.

**Windows XP:** Sem suporte.

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

Examina todos os arquivos do sistema protegidos, mas não repara arquivos.

**Windows XP:** Sem suporte.

</dd> </dl>

O SFC define o seguinte valor do Registro:

 = HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCScan

Para obter mais informações, consulte Valores do Registro [WFP](wfp-registry-values.md).

## <a name="remarks"></a>Comentários

Somente Windows Vista, você pode definir a variável de ambiente **\_ \_ LOGFILE DO WINDOWS TRACING** para o local de um diretório válido para receber um arquivo de log.

## <a name="examples"></a>Exemplos

As linhas de comando de exemplo a seguir são exemplos sfc.exe sintaxe.

**sfc /SCANNOW**

**sfc /VERIFYFILE=c: \\ windows \\ system32 \\kernel32.dll**

**sfc /SCANFILE=d: \\ windows \\ system32 \\kernel32.dll /OFFBOOTDIR=d: \\ /OFFWINDIR=d: \\ windows**

**sfc /VERIFYONLY /FILESONLY**

 

 



