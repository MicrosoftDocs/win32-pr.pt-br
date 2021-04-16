---
description: Você pode especificar um descritor de segurança para um pipe anônimo ao chamar a função CreatePipe. O descritor de segurança controla o acesso às extremidades de leitura e gravação do pipe.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Segurança de pipe anônimo e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758083"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>Segurança de pipe anônimo e direitos de acesso

A segurança do Windows permite que você controle o acesso a Pipes anônimos. Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model).

Você pode especificar um [descritor de segurança](/windows/desktop/SecAuthZ/security-descriptors) para um pipe ao chamar a função [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) . O descritor de segurança controla o acesso às extremidades de leitura e gravação do pipe. Se você especificar **NULL**, o pipe obterá um descritor de segurança padrão. As ACLs no descritor de segurança padrão para um pipe são provenientes do token de representação ou primário do criador.

Para recuperar o descritor de segurança de um pipe, chame a função [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Para alterar o descritor de segurança de um pipe, chame a função [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

A função [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) retorna dois identificadores para o pipe anônimo: um identificador de leitura com \_ acesso genérico de leitura e sincronização; e um identificador de gravação com acesso genérico de \_ gravação e sincronização. \_A leitura genérica e o \_ acesso de gravação genérico usam o mesmo mapeamento de direitos de acesso para pipes nomeados.

\_O acesso de leitura genérico para um pipe anônimo combina os direitos de leitura de dados do pipe, leitura de atributos de pipe, leitura de atributos estendidos e leitura da DACL do pipe.

\_O acesso de gravação genérico para um pipe anônimo combina os direitos de gravar dados no pipe, acrescentar dados a ele, gravar atributos de pipe, gravar atributos estendidos e ler a DACL do pipe.

 

 
