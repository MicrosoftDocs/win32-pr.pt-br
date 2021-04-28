---
description: Revogação de certificado OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revogação de certificado OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092724"
---
# <a name="opm-certificate-revocation"></a>Revogação de certificado OPM

Um certificado do Gerenciador de proteção de saída (OPM) pode ser revogado pela Microsoft. A lista de certificados revogados é armazenada em uma lista de revogação global (GRL). O GRL tem o seguinte formato:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cabeçalho</td>
<td>Uma estrutura de <a href="grl-header.md"><strong>GRL_HEADER</strong></a> .</td>
</tr>
<tr class="even">
<td>Core</td>
<td>Contém as seguintes listas de revogação:
<ul>
<li>Revogações binárias de kernel</li>
<li>Revogações binárias de modo de usuário</li>
<li>Revogações de certificado</li>
<li>Raízes confiáveis (reservadas)</li>
</ul>
A lista de raízes confiáveis não é usada no momento e é reservada para uso futuro.</td>
</tr>
<tr class="odd">
<td>Entradas extensível</td>
<td>Contém informações usadas por outros componentes. Esta seção não é relevante para OPM.</td>
</tr>
<tr class="even">
<td>Renovações</td>
<td>Contém GUIDs que definem Windows Update identificadores. Esta seção contém identificadores para as seguintes listas:
<ul>
<li>Revogações binárias de kernel</li>
<li>Revogações binárias de modo de usuário</li>
<li>Revogações de certificado</li>
</ul>
Um aplicativo pode usar esses identificadores para solicitar uma versão renovada de um binário revogado, se houver um disponível.</td>
</tr>
<tr class="odd">
<td>Assinatura: seção principal</td>
<td>Assina as seções de cabeçalho e núcleo.</td>
</tr>
<tr class="even">
<td>Assinatura: seção extensível</td>
<td>Assina o cabeçalho e as seções extensíveis.</td>
</tr>
</tbody>
</table>



 

O cabeçalho GRL é uma estrutura de [**\_ cabeçalho grl**](grl-header.md) . O membro **dwSequenceNumber** da estrutura contém o número de versão grl. Esse número é incrementado sempre que o GRL é atualizado e uma nova versão colocada no computador do usuário.

Os certificados OPMs revogados são listados na lista de revogações de certificados da seção principal. Cada entrada principal no GRL é uma matriz de 20 bytes que contém o hash SHA-1 da chave pública do certificado revogado.

As seções de assinatura contêm assinaturas que podem ser usadas para verificar se o GRL não foi violado. Cada seção de assinatura contém a estrutura de [**\_ assinatura am MF**](mf-signature.md) . A primeira assinatura assina o cabeçalho mais a seção principal. A segunda assinatura assina o cabeçalho mais a seção extensível; Essa assinatura não é relevante para OPM.

Para garantir que o próprio GRL não tenha sido adulterado, verifique a assinatura da seguinte maneira:

1.  Localize o início da estrutura [**de \_ assinatura MF**](mf-signature.md) . O local da estrutura **de \_ assinatura MF** é fornecido no membro **cbSignatureCoreOffset** da estrutura do [**\_ cabeçalho grl**](grl-header.md) . O local é especificado como um deslocamento em bytes do início do GRL.
2.  Analise a estrutura de [**\_ assinatura MF**](mf-signature.md) como uma \# assinatura PKCS 7 com uma cadeia de certificados.
3.  Verifique a cadeia de certificados para uma raiz confiável.
4.  Verifique se o certificado de folha tem o seguinte identificador de objeto no EKU: "1.3.6.1.4.1.311.10.5.4".
5.  Computar um hash dos bytes que incluem o cabeçalho e as seções principais do GRL.
6.  Verifique se o hash corresponde à assinatura no certificado de folha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> <dt>

[**\_cabeçalho grl**](grl-header.md)
</dt> <dt>

[**\_assinatura MF**](mf-signature.md)
</dt> </dl>

 

 



