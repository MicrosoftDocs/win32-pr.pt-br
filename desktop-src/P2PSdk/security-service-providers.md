---
description: A interface de provedor de serviços de segurança (SSPI) fornece uma interface padrão da indústria para aplicativos distribuídos seguros.
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: Provedores de serviços de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2121940337d0f4e06c53981cf30f0125180c466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757493"
---
# <a name="security-service-providers"></a>Provedores de serviços de segurança

A interface de provedor de serviços de segurança (SSPI) fornece uma interface padrão da indústria para aplicativos distribuídos seguros. A API de grafo de pares fornece uma maneira para que os aplicativos protejam os links em um grafo, especificando um SSP (provedor de serviços de segurança), que é uma DLL que implementa uma interface SSPI. Um aplicativo especifica um SSP quando ele cria um grafo usando [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).

Para obter mais informações sobre como criar seu próprio SSP, consulte o link de documentação SSPI na lista de [links de referência de gráfico](graphing-reference-links.md).

## <a name="programming-considerations-for-implementing-an-ssp"></a>Considerações de programação para implementar um SSP

Tome cuidado ao chamar um aplicativo de dentro de um SSP. As seguintes considerações se aplicam a retornos de chamada do SSP:

-   Os retornos de chamada não devem demorar muito para serem retornados, pois eles são chamados durante a negociação da conexão. Se levar muito tempo para que uma conexão seja estabelecida, a conexão poderá ser descartada.
-   A API de grafo de pares ajusta dinamicamente os valores de tempo limite de conexão, com base na carga real de um sistema. O menor valor de tempo limite é de 20 segundos.
-   Para evitar possíveis situações de deadlock, um aplicativo não deve acessar o banco de dados de grafo de pares de um retorno de chamada. Se um aplicativo exigir informações do banco de dados de gráfico, o aplicativo poderá armazenar em cache as informações necessárias e, em seguida, consultar o cache de dentro do retorno de chamada. O Caching também pode ajudar a diminuir o tempo de conexão.

Ao chamar os pontos de entrada SSPI, a infraestrutura de grafo de pares requer valores específicos para parâmetros específicos de cinco (5) funções. Você não pode alterar esses valores de parâmetro fornecidos para o SSP, e o SSP pode ignorar os valores para os cinco parâmetros ou tratá-los normalmente. A lista a seguir identifica esses parâmetros específicos e os valores necessários:

-   [**Falha AcquireCredentialsHandle**](graphing-reference-links.md)

    Especifique um (1) para o parâmetro *pvGetKeyArgument* . Especifica **NULL** para os parâmetros *pszPrincipal*, *pvLogonID* e *pGetKeyFn* .

-   [**InitializeSecurityContext**](graphing-reference-links.md)

    Especifique os seguintes sinalizadores para o parâmetro *fContextReq* : **ISC \_ req \_ Mutual \_ auth \| ISC \_ req \_ confidenciality ISC req \| \_ \_ Integrity \| ISC \_ req \_ Sequence detectar a \_ \| ISC \_ req \_ Stream \| ISC \_ req \_ alocar \_ memória**.

-   [**AcceptSecurityContext**](graphing-reference-links.md)

    Especifique os seguintes sinalizadores para o parâmetro *fContextReq* : **ASC \_ req \_ Mutual \_ auth \| ASC \_ req \_ confidenciality \| ASC \_ req \_ Integrity \| ASC req \_ \_ Sequence \_ redetect \| ASC \_ req \_ Stream \| ASC \_ req \_ alocar \_ memória**.

-   [**EncryptMessage**](graphing-reference-links.md)

    Especifique zero (0) para os parâmetros *fQOP* e *MessageSeqNo* .

-   [**DecryptMessage**](graphing-reference-links.md)

    Especifique zero (0) para o parâmetro *MessageSeqNo* e **NULL** para o parâmetro *pfQOP* .

Ao chamar [**EncryptMessage**](graphing-reference-links.md), quatro buffers são passados na estrutura **SecBufferDesc** . A tabela a seguir identifica a ordem para passar os buffers.

| Estrutura específica do SSP         | Descrição                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_cabeçalho de fluxo de SECBUFFER \_**  | Contém os dados do cabeçalho de segurança. O tamanho do buffer de cabeçalho é obtido chamando [**QueryContextAttributes**](graphing-reference-links.md) e especificando o atributo **de \_ \_ \_ tamanhos de fluxo de attr SECPKG** .  |
| **dados do SECBUFFER \_**            | Contém a mensagem de texto sem formatação a ser criptografada.                                                                                                                                                                  |
| **\_trailer de fluxo de SECBUFFER \_** | Contém os dados do trailer de segurança. O tamanho do buffer de cabeçalho é obtido chamando [**QueryContextAttributes**](graphing-reference-links.md) e especificando o atributo **de \_ \_ \_ tamanhos de fluxo de attr SECPKG** . |
| **SECBUFFER \_ vazio**           | Não inicializado. O tamanho desse buffer é zero (0).                                                                                                                                                             |



 

Ao chamar [**DecryptMessage**](graphing-reference-links.md), a API de grafo de pares passa exatamente quatro estruturas **SecBuffer** . O primeiro buffer é **SECBUFFER \_ dados** e contém uma mensagem criptografada. Os buffers restantes são usados para saída e são do tipo **SECBUFFER \_ vazio**.

O SSP precisa dar suporte à criptografia e à descriptografia de buffers de dados de usuário com tamanhos de 16K e maior em uma chamada.

 

 



