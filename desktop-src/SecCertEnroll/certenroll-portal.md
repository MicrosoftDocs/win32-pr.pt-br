---
description: Exemplo de certificado. Crie aplicativos para certificação de API, instale o certificado SSL, o certificado do servidor, crie um certificado sobre a mídia, como a Internet ou uma intranet, que não são inerentemente seguras.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501750"
---
# <a name="certificate-enrollment-api"></a>API de registro de certificado

## <a name="purpose"></a>Finalidade

A API de registro de certificado pode ser usada para criar um aplicativo cliente para solicitar um certificado e instalar uma resposta de certificado. Essa API é implementada no CertEnroll.dll a partir do Windows Vista; Ele substitui Xenroll.dll.

## <a name="developer-audience"></a>Público de desenvolvedores

A API de registro de certificado é usada por desenvolvedores de aplicativos que permitirão que os usuários criem, solicitem e recuperem certificados por meio de mídia, como a Internet ou uma intranet, que não são inerentemente seguras. Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++, o COM (Component Object Model) e o ambiente de programação baseado no Windows. Embora não seja necessário, é recomendável compreender a criptografia e a infraestrutura de chave pública.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API de registro de certificado tem suporte a partir do Windows Server 2008 e do Windows Vista. Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre a API de registro de certificado](about-the-certificate-enrollment-api.md)<br/> | Conceitos principais sobre solicitações de certificado são discutidos.<br/>                                                                                                      |
| [Usando a API de registro de certificado](using-the-certificate-enrollment-api.md)<br/> | Como usar a API de registro de certificado para estender os recursos de Active Directory serviços de certificados.<br/>                                              |
| [Referência da API de registro de certificado](certificate-enrollment-api-reference.md)<br/> | Descrições detalhadas de interfaces, enumerações e outros elementos de programação que podem ser usados para registrar um usuário ou computador em uma hierarquia de certificados.<br/> |



 

 

 




