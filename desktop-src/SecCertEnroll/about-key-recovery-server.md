---
description: Uma autoridade de certificação (CA) da Microsoft pode ser configurada para arquivar e recuperar a chave privada associada à chave pública enviada na solicitação de certificado.
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: Servidor de recuperação de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a313ac46bf540d6d0f356f7e2c4910e31bee1f2a4268931ac6a942085505b423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903769"
---
# <a name="key-recovery-server"></a>Servidor de recuperação de chave

Uma autoridade de certificação (CA) da Microsoft pode ser configurada para arquivar e recuperar a chave privada associada à chave pública enviada na solicitação de certificado. A recuperação será útil se uma chave for perdida. Por padrão, somente as chaves de criptografia podem ser arquivadas. Não é necessário arquivar chaves destinadas apenas à assinatura, pois apenas a chave pública é necessária para verificar uma assinatura se a chave de assinatura privada for perdida.

Para arquivar uma chave, a autoridade de certificação deve ser configurada para emitir certificados KRA (agente de recuperação de chave) e para já ter emitido pelo menos um. Um agente de recuperação de chave é um administrador autorizado por uma organização para descriptografar chaves privadas. Para aumentar a segurança, recomendamos que o agente de recuperação de chave e as funções do Gerenciador de certificados sejam atribuídos a indivíduos diferentes, que o Gerenciador de certificados tenha permissão para recuperar, mas não descriptografar chaves arquivadas, e que o agente de recuperação de chave tenha permissão para descriptografar chaves, mas não recuperá-las.

## <a name="key-archival"></a>Arquivamento de chave

Um cliente normalmente solicita um certificado usando um modelo. Se o modelo exigir que a chave privada seja arquivada, as etapas a seguir serão executadas pelo cliente e pela autoridade de certificação:

1.  O cliente recupera e valida o certificado de troca de AC para determinar se ele foi assinado pela mesma chave que foi usada para assinar o certificado de assinatura de autoridade de certificação. Isso garante que a única AC que pode descriptografar a chave privada é a AC da qual um certificado está sendo solicitado.
2.  A chave pública no certificado de troca de AC é usada para criptografar a chave privada associada à solicitação de certificado e a solicitação é enviada para a autoridade de certificação.
3.  A AC usa a chave privada associada ao seu certificado do Exchange para descriptografar a chave privada enviada pelo cliente e verifica se as chaves pública e privada na solicitação estão relacionadas.
4.  A autoridade de certificação criptografa a chave privada usando a chave pública no certificado KRA. Se a AC tiver emitido vários certificados de KRA, ele criptografará a chave privada uma vez com cada chave pública disponível para que qualquer agente de recuperação de chave autorizado possa recuperar uma chave. As chaves privadas criptografadas são armazenadas no banco de dados de certificado.
5.  A CA libera Todas as referências à chave privada e libera com segurança e zera toda a memória que continha a chave. Isso garante que a autoridade de certificação não tenha mais acesso à chave no formato de texto não criptografado.

> [!Note]  
> Somente uma solicitação CMC pode ser usada para arquivamento de chave. As solicitações CMC são representadas pela interface [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

 

## <a name="key-recovery"></a>Recuperação de Chave

Não há suporte direto para a recuperação de chave por Active Directory serviços de certificados ou a API de registro de certificado. No entanto, a Microsoft fornece os seguintes aplicativos para ajudar com o processo:

-   Certutil.exe é um programa de linha de comando que pode ser usado para recuperar informações de configuração de autoridade de certificação, verificar certificados, pares de chaves e cadeias de certificados e fazer backup e restaurar chaves. ele está incluído em sistemas operacionais de servidor que começam com o Windows server 2003.
-   Krecover.exe é um programa baseado na caixa de diálogo que permite a recuperação de chave. ele está incluído no Kit de recursos a partir do Windows Server 2003.

As etapas a seguir são executadas para recuperar uma chave privada:

1.  O Gerenciador de certificados localiza possíveis candidatos à recuperação de chave no banco de dados de certificados usando o nome do certificado, solicitante ou usuário. O comando **certutil** **-GetKey** pode ser usado para essa finalidade.
2.  Depois que o Gerenciador de certificados tiver uma lista de certificados, o comando **-GetKey** será chamado novamente com um número de série de certificado específico ou impressão em miniatura para recuperar um \# arquivo PKCS 7 que contém o certificado kra, a cadeia de certificados do usuário e a chave privada que foi criptografada durante o arquivamento usando a chave pública kra.
3.  O Gerenciador de certificados passa o controle do processo para o agente de recuperação de chave cuja chave privada corresponde à chave pública contida no certificado KRA.
4.  O agente de recuperação de chave descriptografa a chave privada arquivada retornada no \# arquivo PKCS 7 usando a chave privada de Kra. Isso pode ser feito usando o comando **certutil** **-recoverkey** que coloca a chave em um arquivo PKCS 12 protegido por senha \# . O cliente deve receber a senha por meio de um mecanismo fora de banda seguro.
5.  O cliente importa o \# arquivo PKCS 12 e usa a senha para recuperar a chave.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 



