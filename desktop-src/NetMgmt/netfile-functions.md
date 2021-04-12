---
title: Funções de netfile (gerenciamento de rede)
description: As funções de arquivo de gerenciamento de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor. As funções de arquivo são listadas a seguir.
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499217"
---
# <a name="netfile-functions-network-management"></a>Funções de netfile (gerenciamento de rede)

As funções de arquivo de gerenciamento de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor. As funções de arquivo são listadas a seguir.



| Função                                | Descrição                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Força o fechamento de um recurso.                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Retorna informações sobre arquivos abertos em um servidor.                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Retorna informações sobre uma abertura específica de um recurso de servidor. |



 

Chame a função [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) quando o arquivo não puder ser fechado por outros meios. Essa função deve ser usada com cautela porque o **NetFileClose** não grava dados armazenados em cache no sistema cliente para o arquivo antes de fechar o arquivo.

A função [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) retorna informações sobre os recursos abertos em um servidor. Um arquivo pode ser aberto uma ou mais vezes por um ou mais aplicativos. Cada abertura de arquivo é identificada exclusivamente. A função **NetFileEnum** retorna uma entrada para cada abertura de arquivo. A função [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) retorna informações sobre uma abertura de um recurso.

As informações do arquivo estão disponíveis nos seguintes níveis:

-   [**Informações do arquivo \_ \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [**Informações do arquivo \_ \_ 3**](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

Não há suporte para os níveis 0 e 1. O nível 2 retorna apenas o número de identificação atribuído ao recurso quando ele foi aberto. O nível 3 retorna o número de identificação, as permissões, os bloqueios de arquivo e o nome do usuário que abriu o recurso.

Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) . Para obter mais informações, consulte [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
