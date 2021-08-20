---
description: Contém informações que devem identificar exclusivamente o indivíduo que faz a solicitação.
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: Campos de nome distinto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10465a481c1efbaa9637979bb5bb82880451fbe43800b968a4c9fefc5fbc4a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767261"
---
# <a name="distinguished-name-fields"></a>Campos de nome distinto

Uma [*solicitação de certificado*](../secgloss/c-gly.md) contém informações que devem identificar exclusivamente a pessoa que faz a solicitação.

\#As solicitações de certificado de formato PKCS 10 que são aceitas pelos serviços de certificados contêm campos de identificação referenciados como campos de nome distinto (DN). Esses campos conterão as informações que são inseridas pelo usuário quando uma solicitação de certificado está sendo criada pelo Gerenciador de chaves, pelo [controle de registro de certificado](certificate-enrollment-control.md)ou por outros meios.

Veja a seguir algumas diretrizes para a conclusão de campos de DN em uma solicitação de certificado.



| Campo               | Descrição                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome comum         | Certificados de usuário: você deve inserir o nome completo da pessoa. Certificados de máquina: você deve inserir o *caminho do nome de host totalmente qualificado * **/**  usado em pesquisas DNS em que o servidor será executado (por exemplo, *hostname ***.** _Exemplo_* _. com_*).<br/>                                                                                                  |
| Organização        | O nome que você especificar para o campo organização deve ser o nome legal da sua organização que está registrado na autoridade apropriada de cidade, estado ou país/região. O nome legal da organização deve ser usado no campo organização.                                                                                                      |
| Unidade organizacional | O campo de unidade organizacional pode ser usado para diferenciar as diferentes divisões em uma organização, por exemplo "unidade de segurança da Internet" ou "recursos humanos". Esse campo também é recomendado para especificar um valor de DBA (fazendo negócios como...).                                                                                           |
| Localidade            | O campo local indica a cidade em que a organização reside. Se a organização tiver uma posição local apenas, em virtude de ter uma licença de negócios registrada com o administrador da cidade para a cidade de Cambridge no estado de Massachusetts, o campo de localidade deverá conter Cambridge.                                                                |
| Estado ou Província   | O campo Estado ou província especifica onde a organização está localizada fisicamente. Se sua organização for incorporada em Delaware, mas tiver um DBA (fazendo negócios como...) na Califórnia, use a Califórnia. O campo Estado ou província não deve ser um campo Abreviado. Por exemplo, "CA" não é um nome de estado válido. "Califórnia" é o nome do estado adequado. |
| País/região      | O padrão de esquema de nomenclatura [*X. 500*](../secgloss/x-gly.md) requer um código de país/região de 2 caracteres. O código de país/região para o Estados Unidos é US; o código de país/região do Canadá é CA.                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do nome](name-properties.md)
</dt> </dl>

 

 
