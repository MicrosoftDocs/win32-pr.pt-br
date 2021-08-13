---
description: Exemplo de certificado. Crie aplicativos para certificação de API, instale o certificado SSL, o certificado do servidor, crie um certificado pela mídia, como a Internet ou uma intranet, que não são inerentemente seguros.
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: API de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df9caf38f22ac2c8ca8b13e6ca471eea94ae10b5c01ee2da7b4c2247844a70c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902956"
---
# <a name="certificate-enrollment-api"></a>API de registro de certificado

## <a name="purpose"></a>Finalidade

A API de Registro de Certificado pode ser usada para criar um aplicativo cliente para solicitar um certificado e instalar uma resposta de certificado. Essa API é implementada no CertEnroll.dll a partir do Windows Vista; ele substitui Xenroll.dll.

## <a name="developer-audience"></a>Público de desenvolvedores

A API de Registro de Certificado é para uso por desenvolvedores de aplicativos que permitirão que os usuários criem, solicitem e recuperem certificados pela mídia, como a Internet ou uma intranet, que não são inerentemente seguros. Os desenvolvedores devem estar familiarizados com as linguagens de programação C e C++, o COM (Component Object Model) e o ambiente Windows programação baseada em linguagem. Embora não seja necessário, é aconselhável compreender a criptografia e a infraestrutura de chave pública.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API de Registro de Certificado tem suporte a partir do Windows Server 2008 e Windows Vista. Para obter informações sobre os requisitos de tempo de executar para um elemento de programação específico, consulte a seção Requisitos da página de referência para esse elemento.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre a API de Registro de Certificado](about-the-certificate-enrollment-api.md)<br/> | Os principais conceitos sobre solicitações de certificado são discutidos.<br/>                                                                                                      |
| [Usando a API de Registro de Certificado](using-the-certificate-enrollment-api.md)<br/> | Como usar a API de Registro de Certificado para estender os recursos do Serviços de Certificados do Active Directory.<br/>                                              |
| [Referência da API de Registro de Certificado](certificate-enrollment-api-reference.md)<br/> | Descrições detalhadas de interfaces, enumerações e outros elementos de programação que podem ser usados para registrar um usuário ou computador em uma hierarquia de certificados.<br/> |



 

 

 




