---
description: O repositório de certificados é fundamental para todas as operações de gerenciamento de certificados.
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: Estendendo a funcionalidade CertOpenStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c770ae56ff597f51248486db2c9eb2d74bea8d63d2e8daad83d5938594b2f1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007075"
---
# <a name="extending-certopenstore-functionality"></a>Estendendo a funcionalidade CertOpenStore

O [*repositório de certificados*](../secgloss/c-gly.md) é fundamental para todas as operações de gerenciamento de certificados. A funcionalidade da função [**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) pode ser estendida por meio do uso de uma função de provedor de repositório de certificados instalável (ou registrada). Para obter uma visão geral de como instalar ou registrar funções para usar com o CryptoAPI, consulte [visão geral de OID](oid-overview.md).

> [!Note]  
> Os repositórios de certificados personalizados não são migrados automaticamente ao executar implantações automatizadas. para migrar repositórios de certificados personalizados, você deve criar um manifesto para migrar os repositórios personalizados e usar o Ferramenta de Migração do Usuário Windows (USMT). A USMT está disponível para download no centro de download da Microsoft em <https://www.microsoft.com/download/details.aspx?id=10837> .

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) abre um armazenamento vazio na memória e chama a função do provedor de repositório (se estiver registrado ou instalado) usando o OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) que foi passado no parâmetro *lpszStoreProvider* . Para obter uma lista dos tipos de provedor predefinidos que são fornecidos com o CryptoAPI, consulte **CertOpenStore**.

A função de provedor Store copia seus certificados e listas de certificados [*revogados*](../secgloss/c-gly.md) (CRLs) para o repositório na memória especificado pelo identificador *HCERTSTORE* passado para ele. A nova função de provedor de armazenamento pode usar qualquer uma das funções de repositório de certificados CryptoAPI, como [**CertAddCertificateContextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) ou [**CertAddSerializedElementToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore), para adicionar seus certificados e CRLs ao armazenamento na memória. Além disso, a função Store-Provider, opcionalmente, retorna valores para todos os membros de dados da estrutura de [**\_ \_ \_ informações Prov do repositório de certificados**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) . A função só precisa atualizar essa estrutura se ela oferecer suporte a funções de retorno de chamada adicionais. Por exemplo, se o repositório fosse um repositório somente leitura, o suporte de outras funções de retorno de chamada provavelmente não seria necessário. Para obter detalhes e protótipos das funções de retorno de chamada possíveis, consulte [funções de retorno de chamada do provedor de repositório de certificados](cryptography-functions.md).

O repositório TrustedPeople por usuário é restrito a repositórios físicos predefinidos. Você não pode estender o repositório TrustedPeople por usuário. No entanto, você pode estender o repositório TrustedPeople do computador local.

**Windows XP e Windows Server 2003:** O repositório TrustedPeople por usuário não está restrito a repositórios físicos predefinidos.

Um dos membros de dados da estrutura [**de \_ \_ \_ informações Prov do repositório de certificados**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) é a matriz *rgpvStoreProvFunc* . Se a função do provedor de armazenamento precisar dar suporte a uma ou mais das funções de retorno de chamada, ela deverá fornecer ponteiros para essa matriz. Esses ponteiros devem apontar para as funções de retorno de chamada que devem ser usadas para outras atividades do repositório de certificados (como fechar a loja). A ilustração a seguir mostra o fluxo desse processo.

![funcionalidade de CertOpenStore](images/openstor.png)

Conforme mostrado na ilustração a seguir, após a abertura do armazenamento, outras funções de CryptoAPI (como [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)) usam a matriz de ponteiros para acessar as funções de retorno de chamada que executam a tarefa desejada. A definição da estrutura [**de \_ \_ \_ informações Prov do repositório de certificados**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) e os protótipos das funções de retorno de chamada padrão fornecidas com a CryptoAPI são mostradas nas funções de retorno de chamada do provedor de repositório de [certificados](cryptography-functions.md).

![funcionalidade de CertCloseStore](images/closstor.png)

As APIs de armazenamento permitem que um provedor de loja Mantenha os certificados, as CRLs e as [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) fora do cache da loja (por exemplo, um banco de dados externo de certificados, como o fornecido pelo banco de dados do Microsoft Certificate Server).

O [**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) envia por meio do parâmetro *pszStoreProvider* para a função de provedor instalável [**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) apropriada. O provedor retorna informações no parâmetro *pStoreProvInfo* que aponta para uma estrutura [**de \_ \_ \_ informações Prov do repositório de certificados**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) . A estrutura de **\_ \_ \_ informações Prov do repositório de certificados** contém um membro **dwStoreProvFlags** . O \_ sinalizador de sinalizador externo de repositório de certificados \_ Prov \_ \_ foi adicionado para permitir que o provedor indique que os certificados, as CRLs e as CTLs são externas ao cache do armazenamento.

[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) retorna uma matriz de funções de retorno de chamada. Um provedor pode implementar as seguintes funções de retorno de chamada:

-   repositório de certificados \_ \_ Prov \_ fechar \_ Func
-   repositório de certificados \_ \_ Prov \_ Read \_ CERT \_ Func
-   função \_ de \_ \_ certificado de gravação Prov do repositório \_ \_ de certificados
-   repositório de certificados \_ \_ Prov \_ excluir \_ certificado \_ Func
-   \_propriedade de \_ certificado do Prov \_ set CERT \_ \_ Store \_
-   repositório de certificados \_ \_ Prov \_ Read \_ CRL \_ Func
-   função \_ de \_ \_ CRL de gravação Prov \_ do repositório CERT \_
-   repositório de certificados \_ \_ Prov \_ excluir \_ CRL \_ Func
-   repositório de certificados \_ \_ Prov \_ set \_ CRL \_ Property \_ Func
-   repositório de certificados \_ \_ Prov \_ Read \_ CTL \_ Func
-   repositório de certificados \_ \_ Prov de gravação de \_ \_ CTL \_ Func
-   repositório de certificados \_ \_ Prov \_ excluir \_ CTL \_ Func
-   repositório de certificados \_ \_ Prov \_ set \_ CTL \_ Property \_ Func

Em chamadas para as \_ funções de retorno de chamada de cert, Write \_ CRL e Write \_ CTL quando o sinalizador do repositório de certificados \_ \_ Prov \_ Write \_ Add \_ é definido, os 16 bits superiores do parâmetro *dwFlags* contêm o valor *dwAddDisposition* . Para dar suporte a repositórios externos, um provedor pode implementar as seguintes funções de retorno de chamada:

-   repositório de certificados \_ \_ Prov \_ localizar \_ certificado \_ Func
-   repositório de certificados \_ \_ Prov \_ gratuito \_ localizar \_ certificado \_ Func
-   repositório de certificados \_ \_ Prov \_ obter \_ propriedade de certificado \_ \_ Func
-   repositório de certificados \_ \_ Prov \_ localizar \_ CRL \_ Func
-   repositório de certificados \_ \_ Prov \_ gratuito \_ localizar \_ CRL \_ Func
-   \_repositório CERT \_ Prov \_ obter \_ propriedade de CRL \_ \_ Func
-   repositório de certificados \_ \_ Prov \_ localizar \_ CTL \_ Func
-   repositório de certificados \_ \_ Prov \_ gratuito \_ localizar \_ CTL \_ Func
-   \_repositório CERT \_ Prov \_ obter \_ \_ Propriedade CTL \_ Func

As funções de retorno de chamada de certificado têm as seguintes assinaturas:

``` syntax
typedef struct _CERT_STORE_PROV_FIND_INFO {
    DWORD               cbSize;
    DWORD               dwMsgAndCertEncodingType;
    DWORD               dwFindFlags;
    DWORD               dwFindType;
    const void          *pvFindPara;
} CERT_STORE_PROV_FIND_INFO, *PCERT_STORE_PROV_FIND_INFO;
typedef const CERT_STORE_PROV_FIND_INFO CCERT_STORE_PROV_FIND_INFO,
    *PCCERT_STORE_PROV_FIND_INFO;

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_STORE_PROV_FIND_INFO pFindInfo,
        IN PCCERT_CONTEXT pPrevCertContext,
        IN DWORD dwFlags,
        IN OUT void **ppvStoreProvFindInfo,
        OUT PCCERT_CONTEXT *ppProvCertContext
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FREE_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN void *pvStoreProvFindInfo,
        IN DWORD dwFlags
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_GET_CERT_PROPERTY)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN DWORD dwPropId,
        IN DWORD dwFlags,
        OUT void *pvData,
        IN OUT DWORD *pcbData
        );
```

As assinaturas para as funções de retorno de chamada de CRL e CTL são idênticas às anteriores com o ponteiro para o [**\_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) substituído por um ponteiro para um contexto de [**CRL \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) ou um [**\_ contexto de CTL**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context).

O \_ retorno de chamada de certificado Find é chamado quando as APIs de armazenamento enumeram, localizam ou adicionam certificados. *pPrevCertContext* e *ppvStoreProvFindInfo* são definidos como **NULL** para iniciar uma nova localização. O *ppvStoreProvFindInfo* retornado é passado de volta na próxima localização em que a hora em que ele pode ser liberado pelo provedor. O provedor pode definir todas, algumas ou nenhuma das propriedades do certificado. O provedor tem a opção de adiar até que o \_ retorno de chamada da propriedade Get CERT \_ seja chamado. É recomendável que os provedores definam o máximo de propriedades possível para permitir a cópia para outro repositório.

Os tipos de localização de certificado a seguir têm suporte no [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore):

-   \_localizar \_ qualquer certificado
-   CERTIFICADO \_ de \_ encontrar \_ hash SHA1
-   Certificado \_ MD5 de localização de certificados \_ \_
-   \_propriedade de localização de certificado \_
-   \_ \_ chave pública de localização de certificado \_
-   \_nome da \_ entidade de localização do certificado \_
-   \_atributo de localização da \_ entidade de certificado \_
-   \_nome do \_ emissor da localização do certificado \_
-   \_attr do \_ emissor de localização de certificado \_
-   CERTIFICADO \_ de localização da \_ entidade \_ Str \_ A
-   CERTIFICADO de \_ localização da \_ entidade \_ Str \_ W
-   \_o certificado encontrou \_ o emissor \_ \_ A
-   Seq do emissor de localização de certificado \_ \_ \_ \_ W
-   \_especificação de \_ chave de localização de certificado \_
-   CERTIFICADO \_ localizar \_ uso de enhkey \_

O \_ retorno de chamada de certificado Find é chamado para cada um dos tipos de localização acima. Os parâmetros passados para [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) são copiados diretamente para o \_ repositório de certificados \_ Prov \_ localizar a estrutura de \_ informações antes que o retorno de chamada de certificado de localização \_ seja chamado. Para obter detalhes sobre os valores de campo para os diferentes tipos de localização do \_ repositório CERT \_ Prov \_ , encontre a estrutura de \_ informações, consulte **CertFindCertificateInStore**.

Os tipos de localização de certificado a seguir dão suporte às APIs [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) e [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) e ajudam a determinar se o certificado já existe no repositório antes de adicionar:

-   certificado \_ da \_ entidade Localizar certificado \_
-   \_ \_ emissor \_ de localização de certificado de
-   Localização de certificado \_ \_ existente

Para certificado \_ do \_ requerente de localização \_ , o parâmetro *pvFindPara* aponta para uma estrutura de [**\_ informações de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) que contém o emissor e o SerialNumber do assunto. Para \_ \_ o emissor de localização \_ de certificado de, *pvFindPara* aponta para uma estrutura de [**\_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) do assunto. Para \_ Localizar certificado \_ existente, *pvFindPara* aponta para um **\_ contexto CERT** do certificado para verificar sua existência no repositório.

O \_ retorno de chamada de certificado de localização gratuita \_ é chamado quando o certificado retornado pelo retorno de chamada de certificado de localização \_ não foi liberado por estar sendo usado em um próximo certificado de localização posterior \_ , tendo sua [*contagem de referência*](../secgloss/r-gly.md) diminuída para zero ou sendo liberada por uma chamada para [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore). Antes que o retorno de chamada de fechamento seja chamado, todos os certificados retornados pelo retorno de chamada de certificado de localização \_ devem ser liberados para o provedor ao serem passados para uma chamada para o retorno de chamada de \_ certificado Find ou uma chamada para o retorno de chamada de \_ certificado Find gratuito \_ . O mesmo se aplica aos retornos de chamada CRL e CTL.

O \_ retorno de chamada obter propriedade de certificado \_ é chamado por [**CertGetCertificateContextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) se não for possível encontrar a propriedade especificada para o parâmetro *pCertContext* . O mesmo é verdadeiro para obter \_ a \_ propriedade de CRL e obter a \_ \_ Propriedade CTL.

O \_ retorno de chamada Find CRL é chamado quando as APIs de armazenamento enumeram ou obtêm CRLs e antes da adição de uma CRL. Os seguintes tipos de local de CRL serão definidos:

Para CRL \_ FIND \_ ISSUED \_ BY, *pvFindPara* é [**\_**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) um ponteiro para um CONTEXTO DE CERTIFICADO do emissor da CRL. Para CRL \_ FIND \_ EXISTING, *pvFindPara* [**\_**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) é um ponteiro para um CONTEXTO de CRL da CRL para determinar se ela já existe no armazenamento.

O retorno \_ de chamada FIND CTL é chamado quando as APIs do armazenamento enumeram ou encontram CTLs. Os seguintes tipos de encontrar CTL têm suporte [**em CertFindCTLInStore:**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore)

-   CTL \_ FIND \_ ANY
-   CTL \_ FIND \_ SHA1 \_ HASH
-   CTL \_ FIND \_ MD5 \_ HASH
-   USO DE \_ CTL \_ FIND
-   CTL \_ FIND \_ SUBJECT
-   CTL \_ FIND \_ EXISTING

O retorno \_ de chamada FIND CTL é chamado para cada um dos tipos de encontrar acima. Os parâmetros passados [**para CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) são copiados diretamente para a estrutura CERT STORE PROV FIND INFO antes que o retorno de chamada \_ FIND \_ \_ \_ \_ CTL seja chamado. Para obter detalhes sobre os valores de campo para os diferentes tipos de local da estrutura CERT \_ STORE \_ PROV \_ FIND \_ INFO, consulte **CertFindCTLInStore**.

O tipo de encontre CTL EXISTENTE ajuda a determinar se a CTL já existe no armazenamento antes \_ \_ de fazer uma ação de CTL.

Para CTL \_ FIND \_ EXISTING, *pvFindPara* é um ponteiro para a estrutura [**CTL \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) da CTL para determinar se ela já existe no armazenamento.

 

 
