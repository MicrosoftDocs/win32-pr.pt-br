---
description: O arquivo VBScript WiPolicy.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como o script pode ser usado para gerenciar a política do sistema. A política pode ser configurada por um administrador usando o GPE (editor de Política de Grupo).
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Gerenciar configurações de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86684e75e09fa0a588c2d1d0d999488d6e89fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782787"
---
# <a name="manage-policy-settings"></a>Gerenciar configurações de política

O arquivo VBScript WiPolicy.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Este exemplo mostra como o script pode ser usado para gerenciar a [política do sistema](system-policy.md). A política pode ser configurada por um administrador usando o GPE (editor de Política de Grupo).

Este exemplo demonstra as políticas de Windows Installer.

O uso deste exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiPolicy.vbs \[ valor da política \] \[\]**

Se nenhum argumento for especificado na linha de comando, o exemplo retornará as configurações de política atuais. Especifique a política a ser definida usando os códigos de identificador a seguir. Especifique o novo valor para a política. Para retornar o valor atual de uma política, especifique uma cadeia de caracteres vazia "" para o valor.



| CODE | Descrição                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Modos de log. Para obter mais informações, consulte [Logging](logging.md) .                                                                            |
| DO   | Modos de depuração. Para obter mais informações, consulte [debug](debug.md).                                                                                   |
| DI   | Desabilitar o modo de Windows Installer. Para obter mais informações, consulte [DisableMsi](disablemsi.md).                                                      |
| WT   | Tempo limite de espera em segundos no caso de nenhuma atividade. **HKLM** \\ **Software** \\ **Políticas** \\ do **Microsoft** \\ **Windows** \\ **Instalador** \\ do **Tempo limite** |
| DB   | Desabilite a navegação do usuário de locais de origem. Para obter mais informações, consulte [DisableBrowse](disablebrowse.md).                                     |
| DP   | Desabilitar aplicação de patch. Para obter mais informações, consulte [DisablePatch](disablepatch.md).                                                                |
| FICA   | Propriedades públicas enviadas para instalar o serviço. Para obter mais informações, consulte [EnableUserControl](enableusercontrol.md).                             |
| SS   | Instalador seguro para scripts do navegador. Para obter mais informações, consulte [SafeForScripting](safeforscripting.md).                               |
| EM   | Privilégios do sistema (HKLM). Para obter mais informações, consulte [AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| UE   | Privilégios do sistema (HKCU). Para obter mais informações, consulte [AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| DR   | Desabilitar a política de reversão. Para obter mais informações, consulte [DisableRollback](disablerollback.md).                                                   |
| TS   | Localize transformações na raiz da imagem de origem. Para obter mais informações, consulte [TransformsAtSource Policy](transformsatsource-policy.md).             |
| TP   | Fixe o transforma seguro no cache do lado do cliente. Para obter mais informações, consulte [TransformsSecure Policy](transformssecure-policy.md).                 |
| SO   | Ordem de pesquisa de tipos de origem. Para obter mais informações, consulte [SearchOrder](searchorder.md).                                                      |



 

Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 



