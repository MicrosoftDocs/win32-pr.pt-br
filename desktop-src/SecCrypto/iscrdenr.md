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
ms.openlocfilehash: 2471f3acbb483af7e1882102527d392a69e2c7494a929f37718b51a17405c92b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867886"
---
# <a name="iscrdenr-interface"></a>Interface ISCrdEnr

A **interface ISCrdEnr** representa o controle de registro de cartão inteligente. É de interesse principalmente para os desenvolvedores que não usam a Automação. Para programação em Visual Basic ou outra linguagem de Automação, consulte o [**objeto CEnroll.**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))

## <a name="members"></a>Membros

A **interface ISCrdEnr** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCrdEnr** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **interface ISCrdEnr** tem esses métodos.



| Método                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inscrever**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | Solicita um certificado em nome do usuário e armazena o certificado [*resultante*](../secgloss/c-gly.md) no cartão inteligente do [*usuário.*](../secgloss/s-gly.md)<br/>                                                                                                                                                |
| [**enumCAName**](iscrdenr-enumcaname.md)                                 | Enumera os nomes das autoridades de [*certificação*](../secgloss/c-gly.md) (CAs) para um determinado nome de modelo de certificado.<br/>                                                                                                                                                                                                       |
| [**enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)             | Enumera os nomes de modelo de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumCSPName**](iscrdenr-enumcspname.md)                               | Enumera o nome dos CSPs (provedores de [*serviços de criptografia)*](../secgloss/c-gly.md) disponíveis.<br/>                                                                                                                                                                                                               |
| [**getCACount**](iscrdenr-getcacount.md)                                 | Retorna o número de AAs que estão dispostos a emitir um certificado com base no modelo de certificado especificado.<br/>                                                                                                                                                                                                                                                                                                    |
| [**getCAName**](iscrdenr-getcaname.md)                                   | Recupera o nome da AC especificada para um determinado modelo de certificado.<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)             | Recupera o número de modelos de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getCertTemplateName**](iscrdenr-getcerttemplatename.md)               | Recupera o nome do modelo de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getCertTemplateSMIME**](iscrdenr-getcerttemplatesmime.md)             | Determine se um modelo de certificado contém o uso da chave SzOID \_ PKIX \_ KP \_ EMAIL \_ PROTECTION. Se esse uso de chave faz parte do modelo de certificado, o modelo de certificado dá suporte a operações S/MIME (Extensões de [*Internet Mail Seguras/Multipropósitos).*](../secgloss/s-gly.md)<br/> |
| [**getEnrolledCertificateName**](iscrdenr-getenrolledcertificatename.md) | Recupera o nome do certificado resultante de uma chamada bem-sucedida anterior para [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)). Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo.<br/>                                                                                                                                                                                                 |
| [**getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)   | Recupera o nome da assunto do certificado de assinatura. Esse método também pode ser usado para exibir o certificado em uma caixa de diálogo. <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | Recupera o nome do usuário em cujo nome o registro de certificado se destina.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetUser**](iscrdenr-resetuser.md)                                   | Limpa o nome de usuário do controle de cartão inteligente.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)     | Exibe uma caixa **de diálogo Selecionar** Certificado permitindo que um certificado de assinatura (também conhecido como certificado do agente de *registro*) seja selecionado.<br/>                                                                                                                                                                                                                                                           |
| [**selectUserName**](iscrdenr-selectusername.md)                         | Exibe uma caixa **de diálogo Selecionar** Usuário, permitindo que um nome de usuário seja selecionado. O nome de usuário se aplica ao usuário em cujo nome o registro de certificado se destina.<br/>                                                                                                                                                                                                                                     |
| [**setCAName**](iscrdenr-setcaname.md)                                   | Especifica o nome da AC.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setCertTemplateName**](iscrdenr-setcerttemplatename.md)               | Especifica o nome do modelo de certificado.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | Especifica um certificado de assinatura (também conhecido como certificado *do agente de registro*).<br/>                                                                                                                                                                                                                                                                                                                      |
| [**setUserName**](iscrdenr-setusername.md)                               | Especifica o nome do usuário em cujo nome o registro de certificado se destina.<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propriedades

A **interface ISCrdEnr** tem essas propriedades.



| Propriedade                                         | Tipo de acesso           | Descrição                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**CSPCount**](iscrdenr-cspcount.md)<br/> | Somente leitura<br/>  | Especifica o número de CSPs. Esta propriedade é somente para leitura.<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | Leitura/gravação<br/> | O nome do CSP. Essa propriedade é leitura/gravação. <br/>        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr é definido como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



 

 
