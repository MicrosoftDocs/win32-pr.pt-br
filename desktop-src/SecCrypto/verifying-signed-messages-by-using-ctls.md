---
description: Uma das vantagens de usar listas de certificados confiáveis (CTLs) é que os aplicativos podem ser criados para verificar automaticamente as mensagens assinadas em relação a certificados confiáveis sem incomodarr o usuário com caixas de diálogo.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Verificando mensagens assinadas usando CTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760378"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>Verificando mensagens assinadas usando CTLs

Uma das vantagens de usar [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) é que os aplicativos podem ser criados para verificar automaticamente as mensagens assinadas em relação a certificados confiáveis sem incomodarr o usuário com caixas de diálogo. Ele também fornece a confiança de fontes de controle de administrador de rede.

O procedimento a seguir pode ser usado para verificar a assinatura de uma mensagem assinada usando uma CTL.

**Para verificar uma mensagem assinada usando uma CTL**

1.  Decodifique a mensagem da seguinte maneira:

    1.  Obtenha um ponteiro para a mensagem recebida (o [*blob*](../secgloss/b-gly.md)codificado).
    2.  Chame [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passando os argumentos necessários.
    3.  Chame [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) uma vez, passando o identificador recuperado na etapa b e um ponteiro para os dados que serão decodificados. Isso faz com que as ações apropriadas sejam executadas na mensagem, dependendo do tipo de mensagem.

2.  Verifique a assinatura da mensagem decodificada, assinada e obtenha um ponteiro para o [**\_ contexto do certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)do Assinante.

    Isso pode ser feito chamando [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passando o identificador de mensagem recuperado na etapa 1C como o parâmetro *hCryptMsg* . Se a chamada de função retornar **true**, a assinatura foi verificada e um ponteiro para o [**\_ contexto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) do signatário será retornado no parâmetro *ppSigner* .

3.  Confirme se o signatário é uma fonte confiável da seguinte maneira:

    1.  Abra o repositório de certificados que contém a CTL apropriada.
    2.  Obtenha um ponteiro para o [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) chamando [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
    3.  Para confirmar que o signatário é uma fonte confiável, chame [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), passando o ponteiro recuperado na etapa anterior no parâmetro *pCtlContext* , o tipo de \_ \_ entidade de certificado CTL \_ no parâmetro *DwSubjectType* e o ponteiro para o [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) recuperado na etapa 2 no parâmetro *pvSubject* . Se a chamada de função retornar **true**, **o \_ contexto de certificado** passado para a função será uma fonte confiável na CTL.

 

 
