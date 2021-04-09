---
description: Propriedades de nome são propriedades de certificados e solicitações de certificado que representam dados sobre o assunto, ou seja, o proprietário do certificado ou o indivíduo para o qual um certificado é solicitado.
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: Propriedades do nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c5978b3fe5ab7c6ead39840dfb1793372c5feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171482"
---
# <a name="name-properties"></a>Propriedades do nome

Propriedades de nome são propriedades de certificados e solicitações de certificado que representam dados sobre o assunto, ou seja, o proprietário do certificado ou o indivíduo para o qual um certificado é solicitado. Cada propriedade Name é identificada por um nome de propriedade. Esses nomes não são localizáveis; no entanto, as propriedades de nome normalmente correspondem a uma coluna de banco de dados de serviços de certificados, e você pode usar o snap-in do MMC de autoridade de certificação, a ferramenta de linha de comando ' certutil-Schema ' ou o método [**IEnumCERTVIEWCOLUMN:: GetDisplayName**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) para exibir versões localizadas dos nomes de coluna do banco de dados.

O nome da propriedade (mas não os aliases) pode ter "Subject". como um prefixo opcional. Por exemplo, para se referir ao nome comum da entidade, você pode usar "CommonName" ou "Subject. CommonName".

Além de seu nome, cada propriedade tem um número de aliases que os serviços de certificados reconhecem como nomes alternativos para a propriedade. Observe que os [*identificadores de objeto*](../secgloss/o-gly.md) (OIDs) são aliases aceitáveis, assim como as **\_ \* *constantes szOID _. Essas constantes são definições (em Wincrypt. h) que representam os OIDs. Por exemplo, _* szOID \_ \_ nome comum** é definido como "2.5.4.3". Consequentemente, você pode usar as constantes **szOID \_ \** _ como aliases no lugar dos OIDs que representam.



| Nome da propriedade                 | Aliases                                                                                                                                                        | Tipo de dados                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Subject. CommonName"          | "CommonName" "CN"<br/> "2.5.4.3"<br/> _ * szOID \_ \_ nome comum * *<br/>                                                                           | **Cadeia de caracteres** (máx. de 64 caracteres)  | Para certificados de usuário, o nome completo da pessoa. Para certificados de computador, o *caminho hostname * totalmente qualificado **/**  usado em pesquisas de DNS (sistema de nomes de domínio) (por exemplo, *hostname ***.** _Exemplo_* _. com_*).<br/>                                                                                                                                                                                                                                                                        |
| "Assunto. país"             | "País" "C"<br/> "2.5.4.6"<br/> **szOID \_ nome do país \_**<br/>                                                                              | **Cadeia de caracteres** (máximo de 2 caracteres)    | O país ou a região da entidade. Este é um código de país/região de dois caracteres [*X. 500*](../secgloss/x-gly.md) (por exemplo, US para Estados Unidos ou CA para o Canadá).<br/> Muitos desses códigos de dois caracteres são definidos no padrão ISO 3166. Além disso, o código da localidade atual está disponível por meio de uma chamada para a função [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) do Windows (especificando um *LCTYPE* de localidade \_ SISO3166CTRYNAME).<br/> |
| "Subject. DeviceSerialNumber"  | "DeviceSerialNumber" "2.5.4.5"<br/> **\_número de \_ série do dispositivo szOID \_**<br/>                                                                         | **Cadeia de caracteres** (máx. de 1024 caracteres) | Número de série do dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. DomainComponent"     | "DomainComponent" "DC"<br/> "0.9.2342.19200300.100.1.25"<br/> **\_componente de domínio szOID \_**<br/>                                              | **Cadeia de caracteres** (máx. de 128 caracteres)  | Componente de um nome DNS (sistema de nomes de domínio).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.EMail"               | "EMail" "E"<br/> "1.2.840.113549.1.9.1"<br/> **szOID \_ RSA \_ emailAddr**<br/>                                                                  | **Cadeia de caracteres** (máx. de 128 caracteres)  | Endereço de email (por exemplo, " someone@example.com ").                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject. excertoname"           | "Excertoname" "G"<br/> "2.5.4.42"<br/> **szOID \_ \_ nome fornecido**<br/>                                                                             | **Cadeia de caracteres** (máximo de 16 caracteres)   | Nome do assunto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| "Subject.Initials"            | "Iniciais" "I"<br/> "2.5.4.43"<br/> **iniciais do szOID \_**<br/>                                                                                 | **Cadeia de caracteres** (máx. de 5 caracteres)    | Iniciais do assunto (opcional).                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Assunto. localidade"            | "Localidade" "L"<br/> "2.5.4.7"<br/> **\_nome de localidade \_ szOID**<br/>                                                                            | **Cadeia de caracteres** (máx. de 128 caracteres)  | Nome da cidade da entidade.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| "Assunto. organização"        | "Organização" "org."<br/> Minúscula<br/> "2.5.4.10"<br/> **\_nome da organização do szOID \_**<br/>                                                  | **Cadeia de caracteres** (máx. de 64 caracteres)   | Nome legal da organização da entidade.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject. OrgUnit"             | "OrgUnit" "OrganizationUnit"<br/> OrganizationalUnit<br/> CN<br/> 2.5.4.11<br/> **\_nome da \_ unidade \_ organizacional szOID**<br/> | **Cadeia de caracteres** (máx. de 64 caracteres)   | Nome da suborganização ou do departamento da entidade.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Assunto. estado"               | "Estado" "ST"<br/> &<br/> "2.5.4.8"<br/> **\_nome do estado \_ ou \_ província \_ do szOID**<br/>                                                    | **Cadeia de caracteres** (máx. de 128 caracteres)  | Nome completo do Estado ou província da entidade (por exemplo, Califórnia).                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "Subject. StreetAddress"       | "StreetAddress" "Street"<br/> "2.5.4.9"<br/> **Endereço do szOID \_ \_**<br/>                                                                 | **Cadeia de caracteres** (máximo de 30 caracteres)   | Endereço da rua ou caixa postal da entidade.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject. sobrenome"             | "Sobrenome" "SN"<br/> "2.5.4.4"<br/> **szOID \_ \_ nome sur**<br/>                                                                                 | **Cadeia de caracteres** (máx. de 40 caracteres)   | Sobrenome do assunto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Assunto. título"               | "Título" "T"<br/> "2.5.4.12"<br/> **título do szOID \_**<br/>                                                                                       | **Cadeia de caracteres** (máx. de 64 caracteres)   | Título de indivíduo que solicitou o certificado (opcional).                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject. UnstructuredAddress" | "UnstructuredAddress" "1.2.840.113549.1.9.8"<br/> **szOID \_ RSA \_ unstructAddr**<br/>                                                                | **Cadeia de caracteres** (máx. de 1024 caracteres) | Endereço não estruturado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. unstructurename"    | "Unstructurename" "1.2.840.113549.1.9.2"<br/> **szOID \_ RSA não \_ structName**<br/>                                                                   | **Cadeia de caracteres** (máx. de 1024 caracteres) | Nome não estruturado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

As propriedades a seguir estão relacionadas ao assunto, embora não sejam Propriedades de nome. O módulo de política não pode definir essas propriedades diretamente.



| Propriedade                    | Tipo de dados                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Request. DistinguishedName" | **Cadeia de caracteres** (máx. de 8192 caracteres) | O [*nome distinto relativo*](../secgloss/r-gly.md) da solicitação, uma representação textual do assunto na solicitação. Essa representação consiste em Propriedades de nome, por exemplo, "CN = MyName, OU = MyOrgUnit, C = US". O aplicativo de serviços de certificados define essa propriedade antes de chamar o módulo de política, chamando [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) usando o assunto do RawRequest. |
| "Request. RawName"           | **Binary** (máximo de 4096 bytes) | [*Um*](../secgloss/a-gly.md) [*blob*](../secgloss/b-gly.md) de assunto binário (ASN. 1) de uma entidade binária extraído da solicitação. O aplicativo de serviços de certificados define essa propriedade antes de chamar o módulo de política; seu valor é determinado pelo assunto do RawRequest.                                                                                     |
| DistinguishedName         | **Cadeia de caracteres** (máx. de 8192 caracteres) | O nome distinto relativo do certificado, uma representação textual do assunto no certificado. Essa representação consiste em Propriedades de nome, por exemplo, "CN = MyName, OU = MyOrgUnit, C = US". O aplicativo de serviços de certificados define essa propriedade depois de chamar o módulo de política, chamando [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) usando o RawName.                                                                                                               |
| "RawName"                   | **Binary** (máximo de 4096 bytes) | Um [*blob*](../secgloss/b-gly.md) de assunto binário ASN. 1 usado para construir o certificado. O aplicativo de serviços de certificados define essa propriedade depois de chamar o módulo de política; seu valor é determinado pelos valores das propriedades de nome específicas (Subject. CommonName e assim por diante) conforme indicado pelo Subjecttemplate.                                                                                                                                        |



 

Quais componentes de [*nome distinto relativo*](../secgloss/r-gly.md) aparecem na propriedade distinguishedName e a ordem na qual eles aparecem são controlados pelo valor do registro "subjecttemplate" contido na seguinte chave do registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

Quando os serviços de certificados analisam nomes de [*atributos*](../secgloss/a-gly.md) , ele ignora espaços, hifens (sinais de subtração) e maiúsculas e minúsculas. Por exemplo, "AttributeName1", "Attribute Nome1" e "Attribute-Nome1" são equivalentes. Para valores de atributo, os serviços de certificados ignoram espaços em branco à esquerda e à direita.

Todas as propriedades anteriores, exceto DistinguishedName, RawName e Subject. Country, dão suporte à sintaxe de vários valores usando um caractere de nova linha. O separador de nova linha não pode ser desabilitado ou alterado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do certificado](certificate-properties.md)
</dt> <dt>

[**ICertServerExit:: getcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> <dt>

[**ICertServerExit:: requestproperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy:: getcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerPolicy:: requestproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy:: setcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)
</dt> </dl>

 

 
