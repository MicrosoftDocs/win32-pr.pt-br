---
description: O arquivo VBScript WiPolicy.vbs é fornecido nos componentes do SDK do Windows para desenvolvedores Windows instaladores. Este exemplo mostra como o script pode ser usado para gerenciar a política do sistema. A política pode ser configurada por um administrador usando o GPE (Editor Política de Grupo).
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Gerenciar configurações de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1261c48ec7cc7e51a8556b7565075fa9e92bd60481da08f4f311a3de995a91f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945601"
---
# <a name="manage-policy-settings"></a>Gerenciar configurações de política

O arquivo VBScript WiPolicy.vbs é fornecido nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md) Este exemplo mostra como o script pode ser usado para gerenciar a [política do sistema.](system-policy.md) A política pode ser configurada por um administrador usando o GPE (Editor Política de Grupo).

Este exemplo demonstra as políticas Windows do Instalador.

Usar este exemplo requer a versão CScript.exe ou WScript.exe do host Windows Script. Para usar CScript.exe executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for /? ou se poucos argumentos são especificados. Para redirecionar a saída para um arquivo, end end the command line with VBS > \[ *path to file* \] . O exemplo retornará um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiPolicy.vbs \[ de \] \[ política\]**

Se nenhum argumento for especificado na linha de comando, o exemplo retornará as configurações de política atuais. Especifique a política a ser definida usando os códigos de identificador a seguir. Especifique o novo valor para a política. Para retornar o valor atual de uma política, especifique uma cadeia de caracteres vazia "" para o valor.



| CODE | Descrição                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Modos de registro em log. Para obter mais informações, consulte [Registro em log.](logging.md)                                                                            |
| DO   | Modos de depuração. Para obter mais informações, consulte [Depurar](debug.md).                                                                                   |
| DI   | Desabilite Windows do Instalador. Para obter mais informações, [consulte DisableMsi](disablemsi.md).                                                      |
| Wt   | Tempo de espera em segundos no caso de nenhuma atividade. **HKLM** \\ **SoftWare** \\ **Políticas** \\ **Microsoft** \\ **Windows** \\ **Instalador** \\ **Tempo de vida** |
| DB   | Desabilite a navegação do usuário dos locais de origem. Para obter mais informações, [consulte DisableBrowse](disablebrowse.md).                                     |
| DP   | Desabilitar a adoção de patch. Para obter mais informações, consulte [DisablePatch](disablepatch.md).                                                                |
| Uc   | Propriedades públicas enviadas para instalar o serviço. Para obter mais informações, [consulte EnableUserControl](enableusercontrol.md).                             |
| SS   | Instalador seguro para scripts do navegador. Para obter mais informações, [consulte SafeForScripting](safeforscripting.md).                               |
| EM   | Privilégios do sistema (HKLM). Para obter mais informações, [consulte AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| UE   | Privilégios do sistema (HKCU). Para obter mais informações, [consulte AlwaysInstallElevated](alwaysinstallelevated.md).                                      |
| DR   | Desabilite a política de reação. Para obter mais informações, consulte [DisableRollback](disablerollback.md).                                                   |
| TS   | Localize as transformação na raiz da imagem de origem. Para obter mais informações, [consulte TransformsAtSource policy](transformsatsource-policy.md).             |
| TP   | Fixe transformes seguros no cache do lado do cliente. Para obter mais informações, consulte [TransformsSecure policy](transformssecure-policy.md).                 |
| SO   | Ordem de pesquisa dos tipos de origem. Para obter mais informações, consulte [SearchOrder](searchorder.md).                                                      |



 

Para obter exemplos de script adicionais, [consulte exemplos Windows script do instalador.](windows-installer-scripting-examples.md) Para ver os utilitários de exemplo que não exigem Windows Host de Script, consulte Windows Ferramentas de Desenvolvimento [do Instalador](windows-installer-development-tools.md)do .

 

 



