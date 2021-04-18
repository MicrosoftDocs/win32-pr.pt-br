---
description: Quando você abre um identificador para um objeto, o identificador retornado tem alguma combinação de direitos de acesso ao objeto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Solicitando direitos de acesso a um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755965"
---
# <a name="requesting-access-rights-to-an-object"></a>Solicitando direitos de acesso a um objeto

Quando você abre um identificador para um objeto, o identificador retornado tem alguma combinação de direitos de acesso ao objeto. Algumas funções, como [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), não exigem um conjunto específico de direitos de acesso solicitados. Essas funções sempre tentam abrir o identificador para acesso completo. Outras funções, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), permitem que você especifique o conjunto de direitos de acesso que deseja. Você deve solicitar apenas os direitos de acesso de que precisa, em vez de abrir um identificador para acesso completo. Isso impede o uso do identificador de maneira não intencional e aumenta as chances de que a solicitação de acesso seja bem-sucedido se a DACL do objeto permitir acesso limitado.

Use [direitos de acesso genéricos](generic-access-rights.md) para especificar o tipo de acesso necessário ao abrir um identificador para um objeto. Normalmente, isso é mais simples do que especificar todos os direitos padrão e específicos correspondentes. Como alternativa, use a \_ constante máxima permitida para solicitar que o objeto seja aberto com todos os direitos de acesso válidos para o chamador.

> [!Note]  
> A \_ constante máxima permitida não pode ser usada em uma ACE.

 

Para obter ou definir a SACL no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto, solicite o [direito de acesso de \_ \_ segurança do sistema de acesso](sacl-access-right.md) ao abrir um identificador para o objeto.

 

 
