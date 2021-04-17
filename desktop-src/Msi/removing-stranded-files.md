---
description: Uma lista de possíveis motivos pelos quais uma desinstalação do Windows Installer não pôde remover todos os arquivos de um aplicativo.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Removendo arquivos perdidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787495"
---
# <a name="removing-stranded-files"></a>Removendo arquivos perdidos

Se um arquivo que deveria ter sido removido do computador do usuário permanecer instalado após a execução de uma desinstalação, talvez o instalador não esteja removendo o componente que contém o arquivo por um ou mais dos seguintes motivos:

-   O bit msidbComponentAttributesPermanent foi definido para o componente na coluna Attributes da [tabela Component](component-table.md).
-   Nenhum valor foi inserido para o componente na coluna ComponentID da tabela Component.
-   O componente é usado por outro aplicativo ou recurso que ainda está instalado.
-   Há uma condição especificada na tabela de [condição](condition-table.md) que habilita um recurso durante a instalação e desabilita o recurso durante a desinstalação.
-   O arquivo de chave para o componente tem uma contagem de referência anterior em **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   O componente é instalado na pasta System e qualquer arquivo no componente tem uma contagem de referência anterior em **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   O Windows Installer não remove nenhum arquivo ou chave do Registro protegido por [proteção de recursos do Windows](../wfp/windows-resource-protection-portal.md) (WRP). Para obter mais informações, consulte [usando Windows Installer e proteção de recursos do Windows](windows-resource-protection-on-windows-vista.md). No Windows Server 2003, Windows XP e Windows 2000, o instalador não remove nenhum arquivo protegido pela WFP (proteção de arquivo do Windows). Se o arquivo de caminho de chave do componente ou a chave do registro for protegido por WFP ou WRP, o instalador não removerá o componente.
    > [!Note]  
    > Como Windows Installer não instala, atualiza ou remove qualquer recurso protegido por WRP, você não deve incluir recursos protegidos em um pacote de instalação. Em vez disso, use apenas os [mecanismos de substituição de recursos com suporte](../wfp/supported-file-replacement-mechanisms.md) descritos na seção [proteção de recursos do Windows](../wfp/windows-resource-protection-portal.md) .

     

 

 
