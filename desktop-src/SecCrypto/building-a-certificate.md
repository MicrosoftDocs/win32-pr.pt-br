---
description: Explica as chamadas necessárias para criar um certificado.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Criando um certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e497f20e8a20d4e401ce89a85d1f8a312dad76865a6c3dfb523d8f2526125c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772971"
---
# <a name="building-a-certificate"></a>Criando um certificado

A ordem das chamadas na criação de um certificado é a seguinte:

1.  [*A AC*](../secgloss/c-gly.md) (autoridade de certificação) inicializa módulos por meio de chamadas para [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) e [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (ocorre uma vez na inicialização do servidor). A AC inicializa a política e sai dos módulos chamando [**ICertPolicy2::Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) e [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize).
2.  O intermediário chama a AC por meio [**de ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) (ocorre uma vez por inicialização intermediária). O intermediário localiza a cadeia de caracteres de configuração necessária chamando [**ICertConfig::GetConfig.**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig)
3.  O cliente chama o intermediário por meio de uma interface específica para o intermediário (ocorre uma vez por solicitação). O cliente envia [*uma solicitação de*](../secgloss/c-gly.md) certificado para o intermediário. Isso pode ser, por exemplo, o Microsoft Internet Explorer enviar uma solicitação por meio [do](certificate-enrollment-control.md) Controle de Registro de Certificado para Serviços de Informações da Internet da Microsoft.
4.  Intermediário para a AC por meio [**de ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (ocorre uma vez por solicitação). O intermediário envia a solicitação de certificado para a AC por [**meio de ICertRequest::Submit.**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) No caso de Serviços de Informações da Internet, isso pode ser feito por meio de scripts Active Server Pages.
5.  A AC chama o Módulo de Política por meio da interface [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) (ocorre uma vez por solicitação). A AC notifica o módulo de política de que uma solicitação chegou chamando [**ICertPolicy::VerifyRequest.**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) O módulo de política pode examinar a solicitação e alterar o certificado chamando métodos da interface [**ICertServerPolicy.**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) O módulo de política pode indicar que a solicitação está OK (nesse caso, o certificado é criado neste ponto), a solicitação deve ser negada ou a solicitação deve ser suspensa.
6.  (Opcional) O administrador chama a AC por meio da interface [**ICertAdmin.**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) Se a solicitação for suspensa, o administrador poderá reabrir ou negar a solicitação ou modificar atributos e extensões de solicitação. Observe que, se a solicitação for retransmitida, o Módulo de Política terá outra oportunidade para processar a solicitação (como resultado de uma chamada para [**ICertPolicy::VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). A tarefa de resubmitir ou negar a solicitação pode ser executada por meio do snap-in MMC da Autoridade de Certificação ou de outro aplicativo que usa **ICertAdmin**.
7.  A AC chama o módulo exit por meio da interface [**ICertExit.**](/windows/desktop/api/Certexit/nn-certexit-icertexit) Se o módulo de saída tiver indicado (quando [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) foi chamado, na etapa 1) que está interessado em ver certificados emitidos ou solicitações mantidas pendentes, a AC chamará [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify).
8.  O módulo exit chama a AC por meio da interface [**ICertServerExit.**](/windows/desktop/api/Certif/nn-certif-icertserverexit) O módulo de saída pode examinar a solicitação e o novo certificado chamando métodos de **ICertServerExit.**

 

 
