---
description: As funções de arquivo de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor. As funções de arquivo são listadas a seguir.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Funções NetFile (Gerenciamento de Compartilhamento de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efdd1a9339701ccbb534a91b9dfe0423bea546e8d474455c2a6ffdda02adab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362607"
---
# <a name="netfile-functions-network-share-management"></a>Funções NetFile (Gerenciamento de Compartilhamento de Rede)

As funções de arquivo de rede fornecem uma maneira de monitorar e fechar os recursos de arquivo, dispositivo e pipe abertos em um servidor. As funções de arquivo são listadas a seguir.



| Função                                 | Descrição                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | Força o fechamento de um recurso.                                          |
| [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | Retorna informações sobre arquivos abertos em um servidor.                    |
| [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | Retorna informações sobre uma abertura específica de um recurso de servidor. |



 

Chame a [**função NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) quando o arquivo não puder ser fechado por outros meios. Essa função deve ser usada com cuidado porque **NetFileClose** não escreve dados armazenados em cache no sistema cliente no arquivo antes de fechar o arquivo.

A [**função NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) retorna informações sobre os recursos abertos em um servidor. Um arquivo pode ser aberto uma ou mais vezes por um ou mais aplicativos. Cada abertura de arquivo é identificada exclusivamente. A **função NetFileEnum** retorna uma entrada para cada abertura de arquivo. A [**função NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) retorna informações sobre uma abertura de um recurso.

As informações do arquivo estão disponíveis nos níveis a seguir.

<dl>

[**INFORMAÇÕES \_ DO \_ ARQUIVO 2**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[**INFORMAÇÕES \_ DO \_ ARQUIVO 3**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

Não há suporte para os níveis 0 e 1. O nível 2 retorna apenas o número de identificação atribuído ao recurso quando ele foi aberto. O nível 3 retorna o número de identificação, as permissões, os bloqueios de arquivo e o nome do usuário que abriu o recurso.

Se você estiver programando para o Active Directory, poderá chamar determinados métodos ADSI (Interface de Serviço do Active Directory) para obter a mesma funcionalidade que pode obter chamando as funções [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo.**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) Para obter mais informações, [**consulte IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) [**e IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
