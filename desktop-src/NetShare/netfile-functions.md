---
description: As funções de arquivo de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor. As funções de arquivo são listadas a seguir.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Funções de netfile (gerenciamento de compartilhamento de rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df51d556647f16cc30ec51182fde5dd5551831d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757752"
---
# <a name="netfile-functions-network-share-management"></a>Funções de netfile (gerenciamento de compartilhamento de rede)

As funções de arquivo de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor. As funções de arquivo são listadas a seguir.



| Função                                 | Descrição                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | Força o fechamento de um recurso.                                          |
| [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | Retorna informações sobre arquivos abertos em um servidor.                    |
| [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | Retorna informações sobre uma abertura específica de um recurso de servidor. |



 

Chame a função [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) quando o arquivo não puder ser fechado por outros meios. Essa função deve ser usada com cautela porque o **NetFileClose** não grava dados armazenados em cache no sistema cliente para o arquivo antes de fechar o arquivo.

A função [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) retorna informações sobre os recursos abertos em um servidor. Um arquivo pode ser aberto uma ou mais vezes por um ou mais aplicativos. Cada abertura de arquivo é identificada exclusivamente. A função **NetFileEnum** retorna uma entrada para cada abertura de arquivo. A função [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) retorna informações sobre uma abertura de um recurso.

As informações do arquivo estão disponíveis nos seguintes níveis.

<dl>

[**Informações do arquivo \_ \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[**Informações do arquivo \_ \_ 3**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

Não há suporte para os níveis 0 e 1. O nível 2 retorna apenas o número de identificação atribuído ao recurso quando ele foi aberto. O nível 3 retorna o número de identificação, as permissões, os bloqueios de arquivo e o nome do usuário que abriu o recurso.

Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) . Para obter mais informações, consulte [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
