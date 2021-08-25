---
description: Fornece os nomes para identificadores de objeto CAPICOM.
ms.assetid: 6c1eb2cc-84ac-4920-99ba-56ac8de4a851
title: Enumeração de CAPICOM_OID (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_OID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8c008a77e11bd7803dfb09ed2e6ddf1f57ed8695f2de33655239eb73ac49a248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879026"
---
# <a name="capicom_oid-enumeration"></a>Enumeração de OID CAPICOM \_

A enumeração de **\_ OID capicor** fornece os nomes para identificadores de objeto CAPICOM.

Essa enumeração é usada pelo [**OID. Propriedade Name**](oid-name.md) .

## <a name="members"></a>Membros



| Membro                                                        | DESCRIÇÃO                                                                                                                                                                                                                                    | Valor |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_outro OID de CApicom \_**                                       | O objeto não é um dos tipos de objeto CAPICOM predefinidos.<br/>                                                                                                                                                                       | 0     |
| **\_extensão de \_ identificador de chave de autoridade \_ \_ de CAPICOM \_**       | O objeto é uma extensão de certificado que contém o identificador de chave pública da autoridade de certificação (CA).<br/>                                                                                                                  | 1     |
| **\_extensão de \_ atributos de chave \_ \_ capicor OID**                  | O objeto é uma extensão de certificado que contém atributos opcionais de uma chave pública.<br/>                                                                                                                                            | 2     |
| **Extensão de políticas de certificado capicor \_ \_ \_ \_ 95 \_**               | o objeto é uma extensão de certificado que contém informações de política de certificado Windows 95.<br/>                                                                                                                                      | 3     |
| **\_extensão de \_ restrição de uso da chave \_ \_ capicor OID \_**          | O objeto é uma extensão de certificado que contém restrições sobre o uso da chave pública de um certificado.<br/>                                                                                                                          | 4     |
| **\_extensão de \_ \_ \_ mapeamentos de política HERDAdos do \_ capicor OID**         | O objeto é uma extensão de certificado que contém informações de mapeamento de política herdadas.<br/>                                                                                                                                              | 5     |
| **\_extensão do \_ nome da entidade de identificação do \_ \_ capicor \_**               | O objeto é uma extensão de certificado que contém um nome alternativo para o assunto do certificado.<br/>                                                                                                                         | 6     |
| **\_extensão do \_ \_ nome alternativo do emissor de \_ OID \_ do CAPICOM**                | O objeto é uma extensão de certificado que contém um nome alternativo para o emissor do certificado.<br/>                                                                                                                          | 7     |
| **\_extensão de \_ \_ restrições básicas \_ do CAPICOM OID**               | O objeto é uma extensão de certificado que indica se o assunto certificado pode atuar como uma autoridade de certificação, uma entidade final ou ambos. <br/>                                                                                                        | 8     |
| **\_extensão de \_ identificador de chave de entidade \_ \_ capicor OID \_**         | O objeto é uma extensão de certificado que contém o identificador de chave do assunto do certificado.<br/>                                                                                                                           | 9     |
| **\_extensão de \_ uso da chave \_ \_ capicor OID**                       | O objeto é uma extensão de certificado que contém informações sobre o uso pretendido da chave pública de um certificado.<br/>                                                                                                               | 10    |
| **\_extensão do \_ \_ período de \_ uso \_ do CAPICOM PRIVATEKEY**        | O objeto é uma extensão de certificado que contém informações sobre o período de tempo durante o qual a chave privada de um certificado é utilizável.<br/>                                                                                           | 11    |
| **Extensão do CAPICOM \_ \_ Subject \_ ALT \_ nome2 \_**              | O objeto é uma extensão de certificado que contém um nome alternativo para o assunto do certificado.<br/>                                                                                                                         | 12    |
| **Extensão do emissor do capicor \_ \_ \_ ALT \_ nome2 \_**               | O objeto é uma extensão de certificado que contém um nome alternativo para o emissor do certificado.<br/>                                                                                                                          | 13    |
| **Extensão de CONSTRAINTS2 do capico \_ \_ básico \_ \_**              | O objeto é uma extensão de certificado que indica se o assunto certificado pode atuar como uma autoridade de certificação, uma entidade final ou ambos. <br/>                                                                                                        | 14    |
| **\_extensão de \_ restrições de nome de OID de CAPICOM \_ \_**                | O objeto é uma extensão de certificado que contém informações sobre certificados que são especificamente permitidos ou excluídos da relação de confiança.<br/>                                                                                          | 15    |
| **extensão de pontos de distribuição do capicor \_ OID \_ CRL \_ \_ \_**                | O objeto é uma extensão de certificado que contém informações usadas para atualizar a CRL (lista de certificados revogados).<br/>                                                                                                               | 16    |
| **\_extensão de \_ políticas de certificado \_ \_ capicor OID**                   | O objeto é uma extensão de certificado que contém uma lista das políticas às quais o certificado dá suporte.<br/>                                                                                                                           | 17    |
| **\_extensão de \_ \_ mapeamentos de \_ política capicor OID**                 | O objeto é uma extensão de certificado que fornece mapeamentos entre políticas em domínios diferentes.<br/>                                                                                                                                 | 18    |
| **\_Extensão de \_ IDENTIFIER2 de chave de autoridade de identificação de \_ \_ pico \_**      | O objeto é uma extensão de certificado que contém o identificador de chave pública da autoridade de certificação.<br/>                                                                                                                                            | 19    |
| **\_extensão de \_ restrições de política \_ \_ capicor OID**              | O objeto é uma extensão de certificado que contém políticas estabelecidas para aceitar certificados como confiáveis.<br/>                                                                                                                     | 20    |
| **\_extensão de \_ uso avançado de \_ chave \_ \_ de CAPICOM OID**             | O objeto é uma extensão de certificado que contém informações aprimoradas sobre o uso pretendido da chave pública de um certificado.<br/>                                                                                                      | 21    |
| **\_extensão do \_ modelo de certificado \_ \_ capicor OID**            | O objeto é uma extensão de certificado que contém um modelo de certificado.<br/>                                                                                                                                                         | 22    |
| **\_extensão de \_ políticas de certificado de aplicativo \_ \_ capicor OID \_**      | O objeto é uma extensão de certificado que contém a política de aplicativo do certificado.<br/>                                                                                                                                      | 23    |
| **\_extensão de \_ \_ \_ mapeamentos de política de aplicativo \_ capicor OID**    | O objeto é uma extensão de certificado que contém mapeamentos entre diferentes políticas de aplicativo.<br/>                                                                                                                                | 24    |
| **\_extensão de \_ restrições de política de aplicativo \_ \_ capicor OID \_** | O objeto é uma extensão de certificado que contém as restrições de política de aplicativo do certificado.<br/>                                                                                                                          | 25    |
| **\_extensão de \_ acesso de informações da autoridade \_ \_ capicor OID \_**          | O objeto é uma extensão de certificado que indica como acessar informações e serviços de AC para o emissor do certificado.<br/>                                                                                                   | 26    |
| **\_EKU de \_ autenticação de servidor \_ \_ capicor OID**                           | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para autenticar um servidor.<br/>                                                                                                                | 100   |
| **\_EKU de \_ autenticação de cliente \_ \_ capicor OID**                           | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para autenticar um cliente.<br/>                                                                                                                | 101   |
| **\_EKU de \_ assinatura de código \_ \_ capicor OID**                          | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para criar uma assinatura digital.<br/>                                                                                                           | 102   |
| **\_EKU de \_ proteção de email \_ \_ CAPICOM OID**                      | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para proteção de email.<br/>                                                                                                                    | 103   |
| **\_EKU do \_ \_ sistema de extremidade IPSec \_ \_ do capicor OID**                     | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para um sistema de extremidade IPSec.<br/>                                                                                                                 | 104   |
| **\_EKU de \_ \_ túnel IPSec \_ capicor OID**                          | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para túnel IPSec.<br/>                                                                                                                     | 105   |
| **\_EKU de \_ \_ usuário IPSec \_ CAPICOM OID**                            | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para um usuário IPSec.<br/>                                                                                                                       | 106   |
| **EKU de carimbo de data/hora de capicor \_ OID \_ \_ \_**                         | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para o carimbo de data/hora.<br/>                                                                                                                       | 107   |
| **\_EKU de \_ \_ assinatura de \_ uso \_ de identificação de capicor**                    | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para assinar a CTL (lista de certificados confiáveis).<br/>                                                                                                | 108   |
| **\_EKU de \_ \_ assinatura de carimbo de data/hora \_ capicor \_**                   | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para assinar um carimbo de data/hora.<br/>                                                                                                                    | 109   |
| **\_EKU de \_ \_ criptografia restrita do \_ servidor CAPICOM \_**                  | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para a SGC ( [*criptografia de entrada de servidor*](../secgloss/s-gly.md) ).<br/> | 110   |
| **\_EKU de \_ sistema de \_ arquivos \_ com criptografia OID \_ de CAPICOM**               | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para o [*sistema de arquivos com criptografia*](../secgloss/e-gly.md) (EFS).<br/>      | 111   |
| **EKU de recuperação do capicor do \_ \_ EFS \_ \_**                          | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para a recuperação do EFS.<br/>                                                                                                                 | 112   |
| **\_EKU de \_ \_ criptografia de OID do CAPICOM \_**                           | o objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para Windows a criptografia do WHQL (Hardware Quality Labs).<br/>                                                                                   | 113   |
| **\_EKU de criptografia de OID \_ os nt5 \_ \_**                            | o objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para a criptografia Windows Server 2003 e Windows XP.<br/>                                                                                     | 114   |
| **EKU de criptografia do capicor \_ \_ OEM \_ WHQL \_ \_**                      | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para a criptografia WHQL de OEM (fabricantes originais de equipamento).<br/>                                                                            | 115   |
| **\_EKU de \_ criptografia de \_ NT embutido OID \_ de CAPICOM \_**                    | o objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para Windows NT criptografia inserida.<br/>                                                                                                    | 116   |
| **\_EKU do \_ \_ signatário da lista raiz de OID \_ do CAPICOM \_**                     | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para assinar uma lista raiz.<br/>                                                                                                                     | 117   |
| **\_EKU de \_ subordinação qualificada de OID de \_ CAPICOM \_**               | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para subordinação qualificada.<br/>                                                                                                             | 118   |
| **\_EKU de \_ recuperação de chave de OID de CAPICOM \_ \_**                          | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para a recuperação de chave.<br/>                                                                                                                        | 119   |
| **\_EKU de \_ \_ direitos digitais \_ CAPICOM OID**                        | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para direitos digitais.<br/>                                                                                                                      | 120   |
| **\_EKU de \_ licenças de OID capicor \_**                               | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para licenças.<br/>                                                                                                                            | 121   |
| **\_ \_ \_ EKU do servidor de \_ licença capicor OID**                        | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para um servidor de licença.<br/>                                                                                                                    | 122   |
| **\_EKU de \_ \_ logon do cartão inteligente \_ \_ capicor OID**                     | O objeto é um objeto [**EKU**](eku.md) que especifica que o certificado pode ser usado para logon de cartão inteligente.<br/>                                                                                                                    | 123   |
| **\_PKIX do \_ \_ \_ qualificador de \_ política capicor OID**                | O objeto é uma declaração de prática de certificação (CPS) que pode ser usada para o qualificador de política X. 509 (PKIX) da infraestrutura de chave pública.<br/>                                                                                            | 124   |
| **\_WEBnotice \_ do \_ \_ qualificador de política \_ capicor OID PKIX**         | O objeto é um aviso do usuário que pode ser usado para o qualificador de política X. 509 (PKIX) da infraestrutura de chave pública.<br/>                                                                                                                       | 125   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
