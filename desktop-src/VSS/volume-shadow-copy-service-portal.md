---
description: Fazer backup de volumes enquanto os aplicativos em um sistema continuam a gravar nos volumes. Minimize o tempo de inatividade do aplicativo Criando rapidamente um instantâneo (cópia de sombra) de um volume que duplica todos os dados. Execute o backup de multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Serviço de Cópias de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2159d39f407f7ae5dbde454ab6cf3562307d892c
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443077"
---
# <a name="volume-shadow-copy-service"></a>Serviço de Cópias de Sombra de Volume

## <a name="purpose"></a>Finalidade

O Serviço de Cópias de Sombra de Volume (VSS) é um conjunto de interfaces COM que implementa uma estrutura para permitir que os backups de volume sejam executados enquanto os aplicativos em um sistema continuam a gravar nos volumes.

Para obter uma introdução ao VSS para administradores do sistema, consulte [serviço de cópias de sombra de volume](/windows-server/storage/file-server/volume-shadow-copy-service) na biblioteca do TechNet.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O VSS tem suporte no Microsoft Windows XP e versões posteriores. Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da documentação para esse elemento.

Todos os aplicativos VSS de 32 bits (solicitantes, provedores e gravadores) devem ser executados como aplicativos nativos de 32 bits ou de 64 bits. Não há suporte para executá-los em WOW64. Para obter mais informações, consulte [supported Configurations and Restrictions](usage-conventions.md).

**Windows Server 2003 e Windows XP:** A execução de solicitantes do VSS de 32 bits no WOW64 tem suporte, mas não para backups de estado do sistema. Não há suporte para a execução de provedores VSS de 32 bits e gravadores no WOW64. O suporte para a execução de solicitantes de 32 bits no WOW64 foi removido no Windows Vista e em versões posteriores.

> [!Note]  
> Uma cópia de sombra criada no Windows Server 2003 R2 ou no Windows Server 2003 não pode ser usada em um computador que esteja executando o Windows Server 2008 R2 ou o Windows Server 2008. Uma cópia de sombra criada no Windows Server 2008 R2 ou no Windows Server 2008 não pode ser usada em um computador que esteja executando o Windows Server 2003. No entanto, uma cópia de sombra criada no Windows Server 2008 pode ser usada em um computador que esteja executando o Windows Server 2008 R2 e vice-versa.

 

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                          | Descrição                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral](volume-shadow-copy-service-overview.md)<br/> | Descreve o modelo de objeto do VSS, estratégias de backup e restauração e como criar provedores, solicitantes e gravadores do VSS.<br/> |
| [Referência](volume-shadow-copy-reference.md)<br/>       | Descreve classes VSS, tipos de dados, enumerações, funções, interfaces e estruturas.<br/>                                  |



 

## <a name="additional-resources"></a>Recursos adicionais



|   Recurso                                 |   Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista e posterior            | O VSS está disponível no SDK (Software Development Kit) do Microsoft Windows. Você pode instalar o SDK para Windows 7 e Windows Server 2008 R2 no [centro de download do Windows](https://www.microsoft.com/download/details.aspx?id=8279). Você também pode baixar a [versão ISO](https://www.microsoft.com/download/details.aspx?id=8442) do SDK no centro de download do Windows. As versões anteriores do SDK podem ser baixadas na [página de Download SDK do Windows](https://msdn.microsoft.com/windows/bb980924.aspx). |
| Windows Server 2003 e Windows XP | O VSS está disponível no SDK do Serviço de Cópias de Sombra de Volume 7,2, que pode ser baixado no [centro de download do Windows](https://www.microsoft.com/download/details.aspx?id=23490). Observe que os arquivos vssapi. lib de 64 bits nos diretórios no diretório do Win2003 \\ obj podem ser usados para as versões de 64 bits do Windows Server 2003 e do Windows XP.                                                                                                                                                                 |



 

 

 
