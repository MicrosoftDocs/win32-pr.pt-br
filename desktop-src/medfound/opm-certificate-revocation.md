---
description: Revogação de certificado OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revogação de certificado OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b4caeace94f852394081620555c0b5b04918bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478902"
---
# <a name="opm-certificate-revocation"></a>Revogação de certificado OPM

Um certificado OPM (gerenciador de proteção de saída) pode ser revogado pela Microsoft. A lista de certificados revogados é armazenada em uma GRL (lista de revogação global). A GRL tem o seguinte formato:




| Seção | Descrição | 
|---------|-------------|
| Cabeçalho | Uma <a href="grl-header.md"><strong>GRL_HEADER</strong></a> de dados. | 
| Núcleo | Contém as seguintes listas de revogação:<ul><li>Revogações binárias do kernel</li><li>Revogações binárias do modo de usuário</li><li>Revogações de certificado</li><li>Raízes confiáveis (reservadas)</li></ul>Atualmente, a lista de raízes confiáveis não é usada e é reservada para uso futuro. | 
| Entradas extensíveis | Contém informações usadas por outros componentes. Esta seção não é relevante para o OPM. | 
| Renovações: | Contém GUIDs que definem Windows identificadores de atualização. Esta seção contém identificadores para as seguintes listas:<ul><li>Revogações binárias do kernel</li><li>Revogações binárias do modo de usuário</li><li>Revogações de certificado</li></ul>Um aplicativo pode usar esses identificadores para solicitar uma versão renovada de um binário revogado, se um estiver disponível. | 
| Assinatura: seção principal | Assina o header e as seções principais. | 
| Assinatura: seção extensível | Assina o header e as seções extensíveis. | 




 

O header GRL é uma [**estrutura DE \_ HEADER GRL.**](grl-header.md) O **membro dwSequenceNumber** da estrutura contém o número de versão grl. Esse número é incrementado sempre que a GRL é atualizada e uma nova versão é colocada no computador do usuário.

Os certificados OPM revogados são listados na lista de revogações de certificado da seção Core. Cada entrada Core na GRL é uma matriz de 20 byte que contém o hash SHA-1 da chave pública do certificado revogado.

As seções Assinatura contêm assinaturas que podem ser usadas para verificar se a GRL não foi adulterada. Cada seção Assinatura contém a estrutura [**MF \_ SIGNATURE.**](mf-signature.md) A primeira assinatura assina o título mais a seção Core. A segunda assinatura assina o header mais a seção Extensível; essa assinatura não é relevante para o OPM.

Para garantir que a PRÓPRIA GRL não tenha sido adulterada, verifique a assinatura da seguinte maneira:

1.  Local do início da estrutura [**MF \_ SIGNATURE.**](mf-signature.md) O local da **estrutura MF \_ SIGNATURE** é dado no **membro cbSignatureCoreOffset** da estrutura [**GRL \_ HEADER.**](grl-header.md) O local é especificado como um deslocamento em bytes do início da GRL.
2.  Analisar a estrutura [**MF \_ SIGNATURE**](mf-signature.md) como uma assinatura PKCS \# 7 com uma cadeia de certificados.
3.  Verifique a cadeia de certificados até uma raiz confiável.
4.  Verifique se o certificado folha tem o seguinte identificador de objeto na EKU: "1.3.6.1.4.1.311.10.5.4".
5.  Compute um hash dos bytes que incluem o header e as seções principais da GRL.
6.  Verifique se o hash corresponde à assinatura no certificado folha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de Proteção de Saída](output-protection-manager.md)
</dt> <dt>

[**GRL \_ HEADER**](grl-header.md)
</dt> <dt>

[**ASSINATURA \_ MF**](mf-signature.md)
</dt> </dl>

 

 



