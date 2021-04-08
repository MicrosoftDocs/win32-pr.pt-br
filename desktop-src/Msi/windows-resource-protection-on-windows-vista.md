---
description: Windows Installer adere a Proteção de Recursos do Windows (WRP) ao instalar arquivos do sistema, pastas e informações de registro essenciais no Windows Server 2008 e posterior e no Windows Vista e posterior.
ms.assetid: 38865ee1-22ef-430b-99ce-1c6983c3b51f
title: Usando Windows Installer e Proteção de Recursos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72808184ff11b29bfeb02dda576e9393e34189fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921959"
---
# <a name="using-windows-installer-and-windows-resource-protection"></a>Usando Windows Installer e Proteção de Recursos do Windows

Windows Installer adere a Proteção de Recursos do Windows (WRP) ao instalar arquivos do sistema, pastas e informações de registro essenciais no Windows Server 2008 e posterior e no Windows Vista e posterior.

A WRP no Windows Server 2008 e no Windows Vista substitui a WFP (proteção de arquivo do Windows) no Windows Server 2003, no Windows XP e no Windows 2000. Windows Installer os desenvolvedores devem observar as seguintes alterações em como o instalador manipula recursos protegidos no Windows Server 2008 e posterior e no Windows Vista e posterior:

-   Quando executado no Windows Server 2008 e posterior ou no Windows Vista e posterior, o Windows Installer ignora a instalação de qualquer arquivo protegido por WRP, o instalador entra em um aviso no arquivo de log e continua com o restante da instalação sem um erro. No Windows Server 2003, Windows XP e Windows 2000, quando o Windows Installer encontrou um arquivo protegido por WFP, o instalador solicitaria que a WFP instalasse o arquivo.
-   A WRP no Windows Server 2008 e posterior ou no Windows Vista e posterior pode proteger as chaves do registro além dos arquivos. Se o Windows Installer encontrar uma chave de registro protegida por WRP, o instalador ignorará a instalação dessa chave do registro, o instalador inserirá um aviso no arquivo de log e continuará com o restante da instalação sem um erro.
-   Observe que, se um componente de Windows Installer contiver um arquivo ou chave do Registro protegido por WRP, esse recurso deverá ser usado como o caminho principal para o componente. Nesse caso, Windows Installer não instala, atualiza ou remove o componente. Você não deve incluir nenhum recurso protegido em um pacote de instalação. Em vez disso, você deve usar os [mecanismos de substituição de recursos com suporte](../wfp/supported-file-replacement-mechanisms.md) para [proteção de recursos do Windows](../wfp/windows-resource-protection-portal.md).

Para obter mais informações sobre a WRP, consulte [proteção de recursos do Windows](../wfp/windows-resource-protection-portal.md) e informações fornecidas no [Microsoft TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)).

## <a name="wfp-for-windows-server-2003-and-windows-xp2000"></a>WFP para Windows Server 2003 e Windows XP/2000

Windows Installer obedece à WFP (proteção de arquivo do Windows) ao instalar arquivos de sistema essenciais no Windows Server 2003, Windows XP e Windows 2000. Se um arquivo do sistema protegido for modificado por uma instalação autônoma de um aplicativo, a WFP restaurará o arquivo para a versão do arquivo verificado.

Windows Installer nunca tenta instalar ou substituir um arquivo protegido. Quando a ação [InstallFiles](installfiles-action.md) ou qualquer outra ação agendada antes de o InstallFiles tentar instalar um arquivo protegido no windows Server 2003, Windows XP ou Windows 2000, o instalador chama a WFP com uma solicitação para instalar ou substituir o arquivo protegido. O instalador solicita a instalação do arquivo do WFP imediatamente após a execução da ação InstallFiles. A WFP instala ou substitui o arquivo no sistema do usuário por uma versão armazenada em cache do arquivo protegido. Observe que isso não garante que a versão do arquivo instalado do cache seja a versão exigida pelo aplicativo. Depois que o WFP tiver instalado o arquivo, o instalador determinará se essa versão corresponde à versão no pacote. Se a versão do arquivo no pacote for maior que a versão instalada, o instalador informará ao usuário que ele não pode atualizar o sistema e que uma atualização do sistema operacional pode ser necessária para o aplicativo.

Se qualquer ação sequenciada após o [InstallFiles](installfiles-action.md) tentar instalar ou substituir um arquivo protegido ainda não instalado no sistema, o instalador não poderá chamar a WFP para instalar o arquivo. Nesse caso, o instalador informa ao usuário que ele não pode atualizar o sistema e que uma atualização do sistema operacional pode ser necessária para o aplicativo.

O instalador também verifica a WFP ao remover arquivos e nunca tenta remover arquivos protegidos do sistema.

## <a name="component-key-files-protected-by-wfp"></a>Arquivos de chave de componente protegidos por WFP

Observe que, se um componente de Windows Installer contiver um arquivo WFP, esse arquivo deverá ser especificado como o caminho de chave para o componente.

Quando o instalador tenta instalar um arquivo de chave do componente no Windows Server 2003, Windows XP ou Windows 2000, ele chama a WFP primeiro para determinar se o arquivo de chave está protegido. Quando o arquivo de chave de um componente for protegido pela WFP e esse arquivo de chave já estiver instalado, o instalador atualizará o componente somente se a versão do arquivo de chave no pacote for maior do que a versão instalada. Se o pacote de instalação especificar que um componente deve ser instalado e o arquivo de chave do componente não estiver instalado no momento, independentemente de o arquivo de chave estar protegido, o instalador instalará o componente. Depois que qualquer componente que tenha um arquivo de chave protegido pela WFP estiver instalado, ele será instalado permanentemente e o instalador nunca removerá ou substituirá o componente.

## <a name="installation-of-assemblies-by-wfp"></a>Instalação de assemblies por WFP

A WFP para assemblies difere da WFP para arquivos do sistema.

A WFP protege os arquivos do sistema Windows Server 2003, Windows XP e Windows 2000 detectando tentativas de substituição de arquivos protegidos do sistema. Essa proteção é disparada depois que a WFP recebe uma notificação de alteração de diretório para um arquivo em um diretório protegido. Quando a WFP recebe essa notificação, ela determina qual arquivo foi alterado. Se o arquivo estiver protegido, a WFP pesquisará a assinatura do arquivo em um arquivo de catálogo estático para determinar se o novo arquivo é a versão correta. Se a versão do arquivo não estiver correta, o sistema substituirá o arquivo pela versão correta da mídia de cache ou de distribuição.

Por outro lado, a WFP de assemblies é dinâmica. A WFP é estendida para arquivos à medida que são adicionados ao cache de assembly compartilhado lado a lado. Se um assembly for corrompido, a WFP solicitará que o instalador substitua o arquivo. Windows Installer pode ou não ser capaz de substituir o arquivo dependendo se o pacote de origem está acessível. Se o pacote de origem estiver inacessível, a WFP criará uma caixa de diálogo informando que não é possível restaurar o arquivo.

Observe que os assemblies compartilhados lado a lado não gerenciados, instalados em% windir% \\ winsxs, são protegidos pela WFP. Os assemblies privados não gerenciados, instalados no diretório do aplicativo, não são protegidos pela WFP. Os assemblies globais gerenciados instalados no diretório do aplicativo ou no GAC do assembly% windir% \\ \\ não são protegidos pela WFP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Proteção de Recursos do Windows](../wfp/windows-resource-protection-portal.md)
</dt> </dl>

 

 
