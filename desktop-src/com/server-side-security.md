---
title: Segurança de Server-Side
description: Segurança de Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917714"
---
# <a name="server-side-security"></a>Segurança de Server-Side

O servidor pode recuperar informações de segurança sobre um chamador ou representar o chamador usando os métodos de [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity). Uma implementação de **IServerSecurity** é fornecida pelo com no objeto de contexto para a chamada atual quando o empacotamento padrão é usado. No entanto, essa interface pode estar ausente para algumas interfaces com marshaling personalizado.

Quando uma chamada chega ao servidor, o servidor pode chamar [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obter um ponteiro para a interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) . Com esse ponteiro, os métodos **IServerSecurity** podem ser chamados pelo servidor para descobrir quais são as configurações de autenticação do cliente e para representar o cliente, se necessário. O objeto **IServerSecurity** é válido em qualquer thread no apartamento até que a chamada representada por **IServerSecurity** seja concluída. Para obter mais informações sobre representação, consulte [representação](impersonation.md) e [encobrimento](cloaking.md).

As seguintes funções auxiliares que dependem da implementação da interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) do objeto de contexto de chamada também estão disponíveis:

-   [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 