---
title: Errors
description: Esta seção descreve um erro que pode ser emitido por funções de serviços Web do Windows em virtude de uma falha ao executar o comando.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Serviços Web de erros para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822409"
---
# <a name="errors"></a>Errors

Esta seção descreve um erro que pode ser emitido por funções de serviços Web do Windows em virtude de uma falha ao executar o comando.

-   [Parâmetros de saída](#out-parameters)
-   [Códigos de Erro](#error-codes)
-   [Erros avançados](#rich-errors)
-   [Falhas e erros](#faults-and-errors)
-   [Informações de erro sensíveis à linguagem](#language-sensitive-error-information)
-   [Códigos de erro canônicos](#canonical-error-codes)
-   [Uso de API inválido](#invalid-api-usage)
-   [Segurança](#security)

## <a name="out-parameters"></a>Parâmetros de saída

Como regra geral, o valor de parâmetros de saída não será modificado se uma função falhar.

Há algumas instâncias em que parâmetros de saída são modificados se a função falhar. Esses casos são explicitamente chamados na documentação para cada parâmetro. Se a documentação não mencionar nada sobre a modificação de parâmetros em caso de falha, você pode pressupor com segurança que a função não os modificará.

## <a name="error-codes"></a>Códigos de erro

Todos os códigos de retorno de erro são HRESULTs. Essa API define um conjunto de HRESULTs no intervalo de \_ WEBservices de instalação, mas também retorna erros definidos em outro lugar na API do Windows.

Consulte a documentação para obter uma API específica para saber mais sobre quais códigos de erro são retornados. A lista não deve ser exaustiva para cada API, mas sim uma lista de códigos de erro para os quais há cenários comuns de manipulação explícita. Um chamador deve sempre supor que outros códigos de erro sejam possíveis de qualquer API.

Essa API define um número relativamente pequeno de códigos de erro, que correspondem a cenários em que um programa desejará agir com base no erro. Os códigos de erro sozinhos podem não ser suficientes para determinar o que deu errado ou para fornecer uma boa descrição do problema ao usuário. A melhor compreensão do problema vem do uso de erros avançados, conforme descrito abaixo.

## <a name="rich-errors"></a>Erros avançados

Além de retornar um código de erro, um chamador pode opcionalmente solicitar informações de erro ricas para qualquer chamada à API, passando um objeto de [ \_ erro WS](ws-error.md) não **nulo**. Para criar um objeto de erro, use [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror). Se houver um erro, a API que causou o erro preencherá o objeto de erro com contexto adicional sobre a situação de erro. Se não houver nenhum erro, o objeto de erro não será modificado. A passagem de um objeto de erro **nulo** indica que o chamador não está interessado em informações de erro avançadas. Os chamadores (incluindo retornos de chamada) devem estar preparados para lidar com objetos de erro **nulos** .

Observe que o mesmo objeto de erro pode ser usado para várias chamadas de API, mas pode ser usado apenas para uma chamada de API por vez (como é um thread único). Cada vez que ocorre um erro, as informações de erro são acrescentadas ao objeto de erro. Como uma cadeia de chamada se desenrola, várias funções podem adicionar informações ao objeto de erro para fornecer contexto adicional sobre o erro. Para limpar o conteúdo do objeto de erro antes de reutilizá-lo (após ocorrer um erro), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror). Se nenhum erro ocorrer, não será necessário redefinir o objeto de erro antes de reusá-lo.

As informações de erro avançadas consistem no seguinte:

-   Um conjunto de valores de propriedade, que fornece informações adicionais sobre o erro, se presente. Consulte [**\_ \_ propriedade de erro WS**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).
-   Zero ou mais cadeias de caracteres de erro. As cadeias de caracteres são adicionadas usando [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)e podem ser consultadas usando o [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring). O número de cadeias de caracteres pode ser consultado usando a [**\_ \_ \_ \_ contagem de cadeias da propriedade de erro WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="faults-and-errors"></a>Falhas e erros

Confira [falhas](faults.md) para obter informações sobre como os erros e as falhas estão relacionados.

## <a name="language-sensitive-error-information"></a>Informações de erro sensíveis à linguagem

Ao criar um objeto de erro, é especificado o LANGid da tradução de idioma desejada para informações de erro. Isso é usado ao adicionar informações de erro ao objeto de erro.

Esse valor de idioma pode ser recuperado ou definido usando o [**WS \_ Error \_ Property \_ LangID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="canonical-error-codes"></a>Códigos de erro canônicos

Essa API fornece um conjunto canônico de códigos de erro (WS \_ E \_ \* ) que permitem que diferentes tecnologias de comunicação sejam usadas sem precisar depender dos códigos de erro específicos da implementação subjacente específica. Para obter uma lista completa desses códigos de erro, consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md).

Isso permite, por exemplo, que um programa Verifique o código de erro **do \_ ponto de extremidade WS E \_ \_ não \_ encontrado** se estiver usando TCP, UDP ou http e executar alguma ação (como tentar usar um ponto de extremidade diferente).

Quando um código de erro específico de implementação é mapeado para um erro canônico, o código de erro original é salvo no objeto de erro e ainda pode ser acessado para fins de diagnóstico. Consulte [**o \_ \_ código de \_ \_ erro \_ original da propriedade de erro WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) para obter mais informações.

## <a name="invalid-api-usage"></a>Uso de API inválido

Os códigos de erro a seguir são reservados para uso inválido de API e não serão retornados em outras circunstâncias. Se qualquer um desses erros for retornado, ele poderá ser uma indicação de um bug de aplicativo.

-   **\_operação WS E \_ inválida \_**
-   **E \_ INVALIDARG**

As seguintes enumerações fazem parte do rastreamento:

-   [**\_ID da \_ propriedade de erro WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_código de exceção WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Os códigos de erro a seguir fazem parte do rastreamento:

-   **CERT \_ E \_ CN \_ sem \_ correspondência**
-   **CERTIFICADO \_ E \_ expirado**
-   **CERTIFICADO \_ E \_ UNTRUSTEDROOT**
-   **CERTIFICADO \_ E \_ uso incorreto \_**
-   **\_revogação criptografada E \_ \_ offline**
-   **E \_ INVALIDARG**
-   **E \_ OUTOFMEMORY**
-   **\_endereço WS \_ E \_ em \_ uso**
-   **o \_ endereço WS E \_ \_ não \_ está disponível**
-   **\_acesso ao ponto de extremidade WS E \_ \_ \_ negado**
-   **\_ação de ponto de extremidade WS E \_ \_ \_ sem \_ suporte**
-   **\_ponto de extremidade WS E \_ \_ desconectado**
-   **\_falha de \_ ponto de extremidade WS E \_**
-   **\_falha de \_ ponto de extremidade WS E \_ \_ recebida**
-   **\_ponto de extremidade WS E \_ \_ não \_ disponível**
-   **\_ponto de extremidade WS E \_ \_ não \_ encontrado**
-   **\_ponto de extremidade WS E \_ \_ muito \_ ocupado**
-   **\_ponto de extremidade WS E \_ \_ inacessível**
-   **\_URL de \_ ponto de \_ extremidade inválido \_ WS E**
-   **\_ \_ formato inválido de WS E \_**
-   **\_operação WS E \_ inválida \_**
-   **WS \_ E \_ sem \_ suporte**
-   **WS \_ E \_ nenhuma \_ tradução \_ disponível**
-   **\_ \_ estouro numérico de WS E \_**
-   **\_falha no \_ objeto WS E \_**
-   **\_operação WS \_ E \_ abandonada**
-   **\_operação WS \_ E \_ anulada**
-   **a \_ operação WS E \_ \_ atingiu o tempo \_ limite**
-   **\_outros WS E \_**
-   **acesso a proxy do WS \_ E \_ \_ \_ negado**
-   **\_falha de \_ proxy WS E \_**
-   **o \_ proxy WS E \_ \_ requer \_ \_ autenticação básica**
-   **o \_ proxy WS E \_ \_ requer \_ \_ autenticação Digest**
-   **o \_ proxy WS E \_ \_ requer \_ Negotiate \_ auth**
-   **o \_ proxy WS E \_ \_ requer \_ \_ autenticação NTLM**
-   **cota de WS \_ E \_ \_ excedida**
-   **\_ \_ \_ falha no sistema de segurança WS E \_**
-   **TOKEN de segurança do WS \_ E \_ \_ \_ expirado**
-   **\_ \_ \_ falha na verificação de segurança do WS E \_**
-   **o \_ WS \_ E \_ Server \_ requer \_ autenticação básica**
-   **o \_ WS \_ E \_ Server \_ requer \_ autenticação Digest**
-   **o WS \_ E \_ Server \_ requer \_ Negotiate \_ auth**
-   **o \_ WS \_ E \_ Server \_ requer \_ autenticação NTLM**
-   **WS \_ S \_ Async**
-   **fim do WS- \_ S \_**

As funções a seguir fazem parte do rastreamento:

-   [**\_ID da \_ propriedade de erro WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_código de exceção WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

O seguinte identificador é parte do rastreamento:

-   [\_erro WS](ws-error.md)

A seguinte estrutura faz parte do rastreamento:

-   [**\_propriedade de erro WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Segurança

Há várias considerações de segurança que o usuário do objeto de erro deve estar ciente:

-   O objeto de erro pode conter dados não confiáveis. Exemplos disso são: a falha do WS \_ e as cadeias de caracteres de erro, que podem ser armazenadas no objeto de erro com base nas informações recebidas por um canal não confiável. O usuário do objeto de erro deve ser cuidadoso ao inspecionar as informações no objeto de erro e tomar decisões com base em seus valores.
-   Um usuário do objeto de erro deve chamar [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) depois de inspecionar as informações sobre o erro. A falha ao fazer isso pode levar à acumulação de memória.
-   Um usuário do objeto de erro deve ser muito cuidadoso ao usar o \_ valor de \_ \_ divulgação de falha completa do WS da enumeração de [**\_ \_ divulgação de falha do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) , pois a falha gerada pode conter informações privadas que foram acumuladas como parte do processo de gravação de erros.

 

 




