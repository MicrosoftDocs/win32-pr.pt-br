---
description: Lista as interfaces em APIs de autenticação.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfaces de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170032"
---
# <a name="authentication-interfaces"></a>Interfaces de autenticação

As interfaces de autenticação são categorizadas de acordo com o uso da seguinte maneira:

-   [Interfaces de cartão inteligente](#smart-card-interfaces)
-   [Interfaces de compartilhamento de identidade](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>Interfaces de cartão inteligente

O SDK do cartão inteligente fornece as seguintes interfaces COM. Os métodos para uma interface específica são listados no sumário e na página de referência para essa interface.



| Interface                                    | Descrição                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IByteBuffer**](ibytebuffer.md)           | Gerencia um objeto de fluxo.                                                                                                                                                                 |
| [**Iscard**](iscard.md)                     | Abre e gerencia uma conexão com um [*cartão inteligente*](/windows/desktop/SecGloss/s-gly).                                                                    |
| [**ISCardAuth**](iscardauth.md)             | Autentica um aplicativo, um cartão inteligente ou um usuário.                                                                                                                                       |
| [**ISCardCmd**](iscardcmd.md)               | Constrói e gerencia uma APDU ( [*unidade de dados do protocolo de aplicativo*](/windows/desktop/SecGloss/a-gly) de cartão inteligente). |
| [**ISCardDatabase**](iscarddatabase.md)     | Executa operações de banco de dados do [*Gerenciador de recursos*](/windows/desktop/SecGloss/r-gly) de cartão inteligente.                                              |
| [**ISCardFileAccess**](iscardfileaccess.md) | Executa serviços de arquivos comuns, como localizar, selecionar, ler, gravar, criar e excluir arquivos.                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | Constrói um comando APDU.                                                                                                                                                              |
| [**ISCardLocate**](iscardlocate.md)         | Localiza um cartão inteligente.                                                                                                                                                                    |
| [**ISCardManage**](iscardmanage.md)         | Gerencia o sistema de cartão inteligente.                                                                                                                                                           |
| [**ISCardTypeConv**](iscardtypeconv.md)     | Fornece métodos usados para dar suporte a outras interfaces COM de cartão inteligente. Essa interface é fornecida apenas para fins de compatibilidade com versões anteriores e não deve mais ser usada.                               |
| [**ISCardVerify**](iscardverify.md)         | Verifica ou altera a política de verificação do titular do cartão (CHV).                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>Interfaces de compartilhamento de identidade

O SDK de compartilhamento de identidade fornece as seguintes interfaces COM. Os métodos para uma interface específica são listados no sumário e na página de referência para essa interface.



| Interface                                                          | Descrição                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**IAssociatedIdentityProvider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | Permite que um provedor de identidade associe identidades a contas de usuário locais.            |
| [**IIdentityAdvise**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | Permite que um provedor de identidade Notifique um aplicativo de chamada quando uma identidade for atualizada. |
| [**IIdentityprovider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | Representa um provedor de identidade.                                                         |
| [**IIdentityStore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | Fornece métodos para enumerar e gerenciar identidades e provedores de identidade.              |



 

 

 
