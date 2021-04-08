---
description: Explica as chamadas necessárias para criar um certificado.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Criando um certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f237fd729499aa5153f12f68657e2ce227da7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837279"
---
# <a name="building-a-certificate"></a>Criando um certificado

A ordem das chamadas na criação de um certificado é a seguinte:

1.  A CA ( [*autoridade de certificação*](../secgloss/c-gly.md) ) inicializa módulos por meio de chamadas para [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) e [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (ocorre uma vez na inicialização do servidor). A AC inicializará a política e sairá os módulos chamando [**ICertPolicy2:: Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) e [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize).
2.  O intermediário chama a AC por meio de [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) (ocorre uma vez por inicialização intermediária). O intermediário localiza a cadeia de caracteres de configuração necessária chamando [**ICertConfig:: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig).
3.  O cliente chama o intermediário por meio de uma interface específica para o intermediário (ocorre uma vez por solicitação). O cliente envia uma [*solicitação de certificado*](../secgloss/c-gly.md) para o intermediário. Isso pode ser, por exemplo, o Microsoft Internet Explorer enviando uma solicitação por meio do [controle de registro de certificado](certificate-enrollment-control.md) para o Microsoft serviços de informações da Internet.
4.  Intermediário a CA por meio de [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (ocorre uma vez por solicitação). O intermediário envia a solicitação de certificado para a AC por meio de [**ICertRequest:: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit). No caso de Serviços de Informações da Internet, isso pode ser feito por meio de scripts de páginas Active Server.
5.  A CA chama o módulo de política por meio da interface [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) (ocorre uma vez por solicitação). A autoridade de Certificação notifica o módulo de política de que uma solicitação chegou chamando [**ICertPolicy:: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest). O módulo de política pode examinar a solicitação e alterar o certificado chamando métodos da interface [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . O módulo de política pode indicar que a solicitação está OK (se for, o certificado é criado neste ponto), a solicitação será negada ou a solicitação deverá ser suspensa.
6.  Adicional O administrador chama a AC por meio da interface [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) . Se a solicitação for suspensa, o administrador poderá reenviar ou negar a solicitação, ou modificar atributos e extensões de solicitação. Observe que, se a solicitação for reenviada, o módulo de política terá outra oportunidade de processar a solicitação (como resultado de uma chamada para [**ICertPolicy:: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). A tarefa de reenviar ou negar a solicitação pode ser executada por meio do snap-in do MMC da autoridade de certificação ou de outro aplicativo que usa **ICertAdmin**.
7.  A CA chama o módulo de saída por meio da interface [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) . Se o módulo de saída tiver indicado (quando [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) foi chamado, na etapa 1) que está interessado em ver certificados emitidos ou solicitações mantidas pendentes, a autoridade de certificação chamará [**ICertExit:: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify).
8.  O módulo de saída chama a AC por meio da interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) . O módulo de saída pode examinar a solicitação e o novo certificado chamando métodos de **ICertServerExit**.

 

 
