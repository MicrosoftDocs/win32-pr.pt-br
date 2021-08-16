---
description: Explica como criar uma solicitação de certificado e receber e armazenar o certificado retornado em um repositório de certificados.
ms.assetid: 4ca3d6cb-6ce7-4408-9258-6e40c8219dc0
title: Usando o controle de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d489edb7ed288ffc0b51d039c6c32df90631b833d491567729f075c1cee9cae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971753"
---
# <a name="using-certificate-enrollment-control"></a>Usando o controle de registro de certificado

O controle de registro de certificado é um único objeto com muitas propriedades e vários métodos que podem ser usados para determinar como o controle de registro de certificado processa as informações do usuário, o tipo de certificado a ser solicitado, como as chaves devem ser geradas, onde o certificado deve ser armazenado e os processos relacionados. Há dois usos principais do controle de registro de certificado: para criar uma [*solicitação de certificado*](../secgloss/c-gly.md) (PKCS \# 10) e para receber o certificado retornado e armazená-lo em um [*repositório de certificados*](../secgloss/c-gly.md). Para obter detalhes e sintaxe para criar uma instância do objeto de controle de registro de certificado, definir suas propriedades e usar seus métodos, consulte os tópicos a seguir.



| Informações                                                                                                                                                                                           | Tópico                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Criando uma instância do objeto de controle de registro de certificado em diferentes linguagens de programação                                                                                                  | [Criando uma instância do objeto de controle de registro de certificado](creating-an-instance-of-the-certificate-enrollment-control-object.md) |
| Usando propriedades de controle de registro de certificado em diferentes linguagens de programação                                                                                                                    | [Usando as propriedades do controle de registro de certificado](using-the-certificate-enrollment-control-properties.md)                             |
| Coletando as informações necessárias e enviando uma [*solicitação de certificado*](../secgloss/c-gly.md) em diferentes linguagens de programação. | [Criando a solicitação de certificado](creating-the-certificate-request.md)                                                                   |
| Extraindo e armazenando o certificado concluído                                                                                                                                                      | [Recebendo o certificado retornado](receiving-the-returned-certificate.md)                                                               |
| Recuperando informações de valores de retorno em idiomas diferentes                                                                                                                                      | [Valores de retorno do método](method-return-values.md)                                                                                           |
| Verificando se há erros                                                                                                                                                                                   | [Verificação de erros](error-checking.md)                                                                                                       |



 

 

 
