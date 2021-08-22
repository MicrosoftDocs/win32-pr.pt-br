---
description: Windows O instalador segue Windows WRP (Proteção de Recursos) ao instalar arquivos essenciais do sistema, pastas e informações do Registro no Windows Server 2008 e posterior e Windows Vista e posterior.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: Usando Windows instalador e proteção Windows recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ed70b502754dcc54c0954d21e6213d815ba0fa98927f5a67680700a4dd802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012634"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>Usando Windows instalador e proteção Windows recursos

Windows O instalador segue Windows WRP (Proteção de Recursos) ao instalar arquivos essenciais do sistema, pastas e informações do Registro no Windows Server 2008 e posterior e Windows Vista e posterior.

A WRP no Windows Server 2008 e no Windows Vista substitui o WFP (Proteção de Arquivos do Windows) no Windows Server 2003, Windows XP e Windows 2000. Windows Os desenvolvedores do instalador devem observar as seguintes alterações em como o instalador lida com recursos protegidos no Windows Server 2008 e posterior e Windows Vista e posterior:

-   Ao executar no Windows Server 2008 e posterior ou no Windows Vista e posterior, o Instalador do Windows ignora a instalação de qualquer arquivo protegido pela WRP, o instalador inspeções um aviso no arquivo de log e continua com o restante da instalação sem um erro. No Windows Server 2003, Windows XP e Windows 2000, quando o instalador do Windows encontrou um arquivo protegido por WFP, o instalador solicitaria que o WFP instalasse o arquivo.
-   O WRP no Windows Server 2008 e posterior ou Windows Vista e posterior pode proteger chaves do Registro além de arquivos. Se o instalador do Windows encontrar uma chave do Registro protegida por WRP, o instalador ignorará a instalação dessa chave do Registro, o instalador inserirá um aviso no arquivo de log e continuará com o restante da instalação sem erro.
-   Observe que, se um componente Windows Installer contiver um arquivo ou chave do Registro protegido pela WRP, esse recurso deverá ser usado como o KeyPath para o componente. Nesse caso, Windows Instalador não instala, atualiza ou remove o componente. Você não deve incluir nenhum recurso protegido em um pacote de instalação. Em vez disso, você deve usar os [mecanismos de substituição de recursos](../wfp/supported-file-replacement-mechanisms.md) com suporte para Windows Resource [Protection.](../wfp/windows-resource-protection-portal.md)

Para obter mais informações sobre a WRP, [consulte Windows Resource Protection e](../wfp/windows-resource-protection-portal.md) informações fornecidas no Microsoft [Technet.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP para Windows Server 2003 e Windows XP/2000

Windows O instalador segue Windows WFP (Proteção de Arquivos) ao instalar arquivos essenciais do sistema no Windows Server 2003, Windows XP e Windows 2000. Se um arquivo de sistema protegido for modificado por uma instalação autônoma de um aplicativo, o WFP restaurará o arquivo para a versão do arquivo verificado.

Windows O instalador nunca tenta instalar ou substituir um arquivo protegido. Quando a ação [InstallFiles](installfiles-action.md) ou qualquer outra ação agendada antes de InstallFiles tentar instalar um arquivo protegido no Windows Server 2003, Windows XP ou Windows 2000, o instalador chamará o WFP com uma solicitação para instalar ou substituir o arquivo protegido. O instalador solicita a instalação do arquivo do WFP imediatamente após a execução da ação InstallFiles. O WFP instala ou substitui o arquivo no sistema do usuário por uma versão armazenada em cache do arquivo protegido. Observe que isso não garante que a versão do arquivo instalado do cache seja a versão exigida pelo aplicativo. Depois que o WFP tiver instalado o arquivo, o instalador determinará se essa versão corresponde à versão no pacote. Se a versão do arquivo no pacote for maior que a versão instalada, o instalador informará ao usuário que ele não pode atualizar o sistema e que uma atualização do sistema operacional pode ser necessária para o aplicativo.

Se qualquer ação sequenciada após [InstallFiles](installfiles-action.md) tentar instalar ou substituir um arquivo protegido ainda não instalado no sistema, o instalador não poderá chamar o WFP para instalar o arquivo. Nesse caso, o instalador informa ao usuário que ele não pode atualizar o sistema e que uma atualização do sistema operacional pode ser necessária para o aplicativo.

O instalador também verifica com o WFP ao remover arquivos e nunca tenta remover arquivos do sistema protegidos.

## <a name="component-key-files-protected-by-wfp"></a>Arquivos de chave de componente protegidos pelo WFP

Observe que, se um Windows instalador contiver um arquivo WFP, esse arquivo deverá ser especificado como o caminho da chave para o componente.

Quando o instalador tenta instalar o arquivo de chave de um componente no Windows Server 2003, no Windows XP ou no Windows 2000, ele primeiro chama o WFP para determinar se o arquivo de chave está protegido. Quando o arquivo de chave de um componente é protegido pelo WFP e esse arquivo de chave já está instalado, o instalador atualiza o componente somente se a versão do arquivo de chave no pacote for maior que a versão instalada. Se o pacote de instalação especificar que um componente será instalado e o arquivo de chave do componente não estiver instalado no momento, independentemente de o arquivo de chave estar protegido, o instalador instalará o componente. Depois que qualquer componente que tenha um arquivo de chave protegido pelo WFP for instalado, ele será instalado permanentemente e o instalador nunca removerá ou substituirá o componente.

## <a name="installation-of-assemblies-by-wfp"></a>Instalação de assemblies por WFP

O WFP para assemblies difere do WFP para arquivos do sistema.

O WFP protege Windows Server 2003, Windows XP e Windows do sistema 2000 detectando tentativas de substituir arquivos do sistema protegidos. Essa proteção é disparada depois que o WFP recebe uma notificação de alteração de diretório para um arquivo em um diretório protegido. Quando o WFP recebe essa notificação, ele determina qual arquivo foi alterado. Se o arquivo estiver protegido, o WFP procura a assinatura do arquivo em um arquivo de catálogo estático para determinar se o novo arquivo é a versão correta. Se a versão do arquivo não estiver correta, o sistema substituirá o arquivo pela versão correta do cache ou da mídia de distribuição.

Por outro lado, o WFP de assemblies é dinâmico. O WFP é estendido para arquivos conforme eles são adicionados ao cache de assembly lado a lado compartilhado. Se um assembly ficar corrompido, o WFP solicitará que o instalador substitua o arquivo. Windows O instalador pode ou não ser capaz de substituir o arquivo dependendo se o pacote de origem está acessível. Se o pacote de origem estiver inacessível, o WFP colocará uma caixa de diálogo informando que não é possível restaurar o arquivo.

Observe que assemblies compartilhados não planejados lado a lado, instalados em %windir% \\ winsxs, são protegidos pelo WFP. Assemblies privados nãomanagedos, instalados no diretório do aplicativo, não são protegidos pelo WFP. Assemblies globais gerenciados instalados no diretório do aplicativo ou %windir% do assembly gac não \\ são \\ protegidos pelo WFP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Proteção de recursos](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
