---
description: Representa o controle de registro de cartão inteligente.
ms.assetid: ae872206-81e7-4627-b807-4222f75f8ab6
title: Interface ISCrdEnr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 3c3c882020db8b25c587a8d95824b3c90232bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753398"
---
# <a name="iscrdenr-interface"></a>Interface ISCrdEnr

A interface **ISCrdEnr** representa o controle de registro de cartão inteligente. É basicamente interessante que os desenvolvedores não usem a automação. Para a programação em Visual Basic ou outra linguagem de automação, consulte o objeto [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) .

## <a name="members"></a>Membros

A interface **ISCrdEnr** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCrdEnr** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **ISCrdEnr** tem esses métodos.



| Método                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Registr**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | Solicita um certificado em nome do usuário e armazena o [*certificado*](../secgloss/c-gly.md) resultante no [*cartão inteligente*](../secgloss/s-gly.md)do usuário.<br/>                                                                                                                                                |
| [**enumCAName**](iscrdenr-enumcaname.md)                                 | Enumera os nomes das autoridades de [*certificação*](../secgloss/c-gly.md) (CAS) para um determinado nome de modelo de certificado.<br/>                                                                                                                                                                                                       |
| [**enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)             | Enumera os nomes de modelo de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumCSPName**](iscrdenr-enumcspname.md)                               | Enumera o nome dos CSPs ( [*provedores de serviço de criptografia*](../secgloss/c-gly.md) ) disponíveis.<br/>                                                                                                                                                                                                               |
| [**getCACount**](iscrdenr-getcacount.md)                                 | Retorna o número de CAs que desejam emitir um certificado com base no modelo de certificado especificado.<br/>                                                                                                                                                                                                                                                                                                    |
| [**getCAName**](iscrdenr-getcaname.md)                                   | Recupera o nome da autoridade de certificação especificada para um determinado modelo de certificado.<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)             | Recupera o número de modelos de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getCertTemplateName**](iscrdenr-getcerttemplatename.md)               | Recupera o nome do modelo de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getCertTemplateSMIME**](iscrdenr-getcerttemplatesmime.md)             | Determine se um modelo de certificado contém o \_ uso da chave de proteção de email szOID PKIX \_ KP \_ \_ . Se esse uso de chave fizer parte do modelo de certificado, o modelo de certificado dará suporte a operações de S/MIME ( [*Internet Mail Extensions) seguras/multipropósitos*](../secgloss/s-gly.md) .<br/> |
| [**getEnrolledCertificateName**](iscrdenr-getenrolledcertificatename.md) | Recupera o nome do certificado resultante de uma chamada bem-sucedida anterior para [**ISCrdEnr:: inscrever**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)). Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo.<br/>                                                                                                                                                                                                 |
| [**getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)   | Recupera o nome da entidade do certificado de autenticação. Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo. <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | Recupera o nome do usuário em cujo nome o registro de certificado é pretendido.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetUser**](iscrdenr-resetuser.md)                                   | Limpa o nome de usuário do controle de cartão inteligente.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)     | Exibe uma caixa de diálogo **Selecionar certificado** que permite que um certificado de autenticação (também conhecido como o *certificado do agente de registro*) seja selecionado.<br/>                                                                                                                                                                                                                                                           |
| [**selectUserName**](iscrdenr-selectusername.md)                         | Exibe uma caixa de diálogo **Selecionar usuário** , permitindo que um nome de usuário seja selecionado. O nome de usuário se aplica ao usuário em cujo nome o registro de certificado é pretendido.<br/>                                                                                                                                                                                                                                     |
| [**setCAName**](iscrdenr-setcaname.md)                                   | Especifica o nome da autoridade de certificação.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setCertTemplateName**](iscrdenr-setcerttemplatename.md)               | Especifica o nome do modelo de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | Especifica um certificado de autenticação (também conhecido como o *certificado do agente de registro*).<br/>                                                                                                                                                                                                                                                                                                                      |
| [**SetUserName**](iscrdenr-setusername.md)                               | Especifica o nome do usuário em cujo nome o registro de certificado é pretendido.<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propriedades

A interface **ISCrdEnr** tem essas propriedades.



| Propriedade                                         | Tipo de acesso           | Descrição                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**CSPCount**](iscrdenr-cspcount.md)<br/> | Somente leitura<br/>  | Especifica o número de CSPs. Esta propriedade é somente para leitura.<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | Leitura/gravação<br/> | O nome do CSP. Esta propriedade é de leitura/gravação. <br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



 

 
